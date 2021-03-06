# Image Colorization Starter Code
The objective is to produce color images given grayscale input image. 

## Setup Instructions
Create a conda environment with pytorch, cuda. 

`$ conda install pytorch torchvision torchaudio cudatoolkit=11.1 -c pytorch -c nvidia`

For systems without a dedicated gpu, you may use a CPU version of pytorch.
`$ conda install pytorch torchvision torchaudio cpuonly -c pytorch`

## Dataset
Use the zipfile provided as your dataset. You are expected to split your dataset to create a validation set for initial testing. Your final model can use the entire dataset for training. Note that this model will be evaluated on a test dataset not visible to you.

## Code Guide
Baseline Model: A baseline model is available in `basic_model.py` You may use this model to kickstart this assignment. We use 256 x 256 size images for this problem.
-	Fill in the dataloader, (colorize_data.py)
-	Fill in the loss function and optimizer. (train.py)
-	Complete the training loop, validation loop (train.py)
-	Determine model performance using appropriate metric. Describe your metric and why the metric works for this model? 
- Prepare an inference script that takes as input grayscale image, model path and produces a color image. 

## Additional Tasks 
- The network available in model.py is a very simple network. How would you improve the overall image quality for the above system? (Implement)
- You may also explore different loss functions here.

## Bonus
You are tasked to control the average color/mood of the image that you are colorizing. What are some ideas that come to your mind? (Bonus: Implement)

## Solution
- Document the things you tried, what worked and did not. 
- Update this README.md file to add instructions on how to run your code. (train, inference). 
- Once you are done, zip the code, upload your solution.  

## Instructions
- The Jupiter notebook Colorization.ipynb contains the solution.
- The architecture of the best model is described in the class Net2.
- The input of the models for training should be a representative of the class ColorizeData uploaded into the dataloader.
- Parameters of the basic and final models are located within the files "weights.pth" and "weights2.pth" respectively and should be uploaded before inference (the code for that is inside the cells immediately before the training cells).
- All the commentaries are in markdown cells in the .ipynb file.
- All the necessary files (such as "weights.pth" and "weights2.pth") are located in the .zip archive.
- There are some examples of the inference in the notebook as well as the preprocessing of the training and validation sets.
- The function "inference" accepts the model and an image as a numpy array and returns colorized image-tensor
