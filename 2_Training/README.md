# TrainYourOwnYOLO: Training
Using the training images located in [`TrainYourOwnYOLO/Data/Source_Images`](/Data/Source_Images) and the annotation file [`data_train.txt`](/Data/Source_Images/vott-csv-export) which we have created in the [previous step](/1_Image_Annotation/) we are now ready to train our YOLOv3 detector. 

## Download the Pre-Trained Weights
Before getting started we need to download the pre-trained YOLOv3 weights and convert them to the keras format. To run both steps execute:

```
python Download_and_Convert_YOLO_weights.py
```
## Train YOLOv3 Detector
To start the training run the training script:
```
python Train_YOLO.py 
```
Depending on your set-up this process can take a few minutes to a few hours. I recommend using a GPU to speed up training. The final weights are saved in [`TrainYourOwnYOLO/Data/Model_weights`](/Data/Model_weights). 

### Training on AWS
If training is too slow on your local machine, you can speed up the training by using a GPU cluster on AWS. To learn more about training on AWS navigate to the [`AWS`](/2_Training/AWS) folder.

This concludes the training step and you are now ready to detect cat faces in new images!