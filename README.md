# Yang and Justin Computer Vision Final Project
This is the repo of the Yang and Justin's final project for computer vision class. We aim to develop a trained model for classfing whether a dog is have anxiety or not. There are 3 stages of our project: data acquisition, model training, and app development.

# Data Acquisition(Yang)
We use youtube-dl to download videos from YouTube(Command line):

```
youtube-dl [OPTIONS] URL [URL...]
```


We then use scenedetect to convert input videos to output images(Command line):
```
scenedetect -i video.mp4 detect-content save-images
```

Finally, we manually select those images that actually have a dog inside.

# Model Training(Justin)
In progress

# App development
