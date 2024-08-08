# Basic-Flag-Detector

Basic Flag Detector (Mexico, U.S, Pakistan)


 The model uses trained the algorithim and testing image classification models on the NVIDIA Jetson Nano.

 Running this Project
 1. Testing the Model:
 Enter the jetson-inference/python/training/classification directory:

#### cd jetson-inference/python/training/classification

 Set the NET and DATASET variables:
 Copy code (ONE AT A TIME)

#### NET=models/flags
#### DATASET=data/flags

 Run the image classification script

 Mexico
#### imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/Mexico/11447.png output.png


 Pakistan
#### imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/Pakistan/151.png output.png

 United States
#### imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/United-States/2283.png output.png



#### 2. Review Results:
#### Observe the output image (outcome.png) to evaluate the classification results. The accuracy depends on the number of epochs and the quality of the dataset.

#### Video link
#### https://drive.google.com/file/d/19eA_DcfTlTHgdy-PlBHC9HgK7Ek3ocsu/view?usp=sharing
