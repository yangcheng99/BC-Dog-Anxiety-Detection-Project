# Yang and Justin Computer Vision Final Project
This is the repo of the Yang and Justin's final project for computer vision class. We aim to develop a trained model for classfing whether a dog is have anxiety or not. There are 3 stages of our project: data acquisition, model training, and app development.

# Data Acquisition(Yang)
Our goal is to produce a training set of images consist of normal dogs and anxious dogs. To do that, we use Youtube videos as the source of out dataset. We then convert videos into images with scene detection. Finally, we select images that have dogs inside with ResNet-50.

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

Finally, we select those images that have a dog inside with ResNet-50. I used pretrained ResNet_50 weights in keras to detect dog from images. If the predicted class of ResNet50 on ImageNet falls into the dog breed categories dog detector, we classify the input image as a dog image and keep it. Otherwise, we discard it from our dataset. See details in the ipynb file.

# Model Training(Justin)
In progress

# App development
