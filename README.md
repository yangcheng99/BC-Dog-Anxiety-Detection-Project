# Dog Anxiety Detection Project
This is the repo of dog anxiety detection app developed by BC computer vision group.. We aim to develop a trained model for classfing whether a dog is having anxiety or not. There are 3 stages of our project: data acquisition, model training, and app development.



# Data Acquisition(Yang)
Our goal is to produce a training set of images consist of normal dogs and anxious dogs. To do that, we use Youtube videos as the source of out dataset. We then convert videos into images with scene detection. Finally, we select images that have dogs inside with ResNet-50.

#Package Dependencies
```
Python 3.5
Pytorch
OpenCV
scenedetect
tqdm
```
# Step 1:
Input: URL; Output: Videos

We use youtube-dl to download videos from YouTube (Command line):

```
youtube-dl [OPTIONS] URL [URL...]
```

# Step 2:
Input: Videos; Output: Distinct frames as different images.

We then use scenedetect to convert input videos to output images. Since we need to compare consective frames, we need to use the method "detect-content". This can be done through (Command Line):
```
scenedetect -i video.mp4 detect-content save-images
```

# Step 3:
Input: Images; Output: Images with dog inside.

Finally, we select those images that have a dog inside with ResNet-50. I used pretrained ResNet_50 weights in keras to detect dog from images. If the predicted class of ResNet50 on ImageNet falls into the dog breed categories, the dog detector classify the input image as a dog image and keep it. Otherwise, we discard it from our dataset. See details in the ipynb file.

# Model Training(created by Huidong Hou)
The MVP version is listed, as this is the minimum version that can predict the binary classification, anxious vs. Normal. 
The code was written using pytorch but will be converted using tensorflow, stay tuned!
The second generation is to have a probabalistic determination, instead of a simple binary classification, I am still developing!
