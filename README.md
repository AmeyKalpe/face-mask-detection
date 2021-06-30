# face-mask-detection
A system that detects whether a person is wearing a face mask or not.

<b> The system can be initialized by executing the detect_mask_video.py script, which will use the camera available on the machine executing the script. </b>

The system uses MobileNetV2 architecture, which is a pre-trained CNN model consisting of 53 layers trained on ImageNet dataset, as the backend framework.

The deep learning model is trained on images with labels as 'with_mask' and 'without_mask', 'with_mask' class consisting of 4150 images and 'without_mask' class consisting of 4195 images. The model is then saved onto disk and loaded during the detection phase.

The dataset can be downloaded using <a href="https://drive.google.com/file/d/1VQoy3K6fUCY2F-SChhk3mO4-CrytBdCc/view?usp=sharing" target="_blank">this link</a>.

The detection is done over the live video stream using OpenCV library, first extracting the Region of Interest, and then performing mask detection using the deployed model.

The person wearing a face mask is indicated by a green rectangle around the face of that person, while a red rectangle is displayed around the face of a person not wearing a face mask. Moreover, the detection does not start until a person is in front of the camera, until then, a message "No faces detected" is displayed.

The system has been trained on images with people wearing masks partially and the training parameters are optimized as well, which helps to classify people wearing masks partially into the "without_mask" category.

Output Results:

![image](https://user-images.githubusercontent.com/56644208/123783639-36ec2e80-d8f4-11eb-9c97-e66cd7e80dc0.png)

![image](https://user-images.githubusercontent.com/56644208/123783662-3ce20f80-d8f4-11eb-8e50-f846f7d93479.png)

![image](https://user-images.githubusercontent.com/56644208/123783686-466b7780-d8f4-11eb-9b1c-b8b16e595b29.png)

![image](https://user-images.githubusercontent.com/56644208/123783714-4c615880-d8f4-11eb-81df-38c9a0723562.png)

