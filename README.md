# face-mask-detection
A system that detects whether a person is wearing a face mask or not.

<b> The system can be initialized by executing the detect_mask_video.py script, which will use the camera available on the machine executing the script. </b>

The system uses MobileNetV2 architecture, which is a pre-trained CNN model consisting of 53 layers trained on ImageNet dataset, as the backend framework.

The deep learning model is trained on images with labels as 'with_mask' and 'without_mask', 'with_mask' class consisting of 4150 images and 'without_mask' class consisting of 4195 images. The model is then saved onto disk and loaded during the detection phase.

The dataset can be downloaded using <a href="https://drive.google.com/file/d/1VQoy3K6fUCY2F-SChhk3mO4-CrytBdCc/view?usp=sharing" target=_blank>this link</a>.

The detection is done over the live video stream using OpenCV library, first extracting the Region of Interest, and then performing mask detection using the deployed model.

The person wearing a face mask is indicated by a green rectangle around the face of that person, while a red rectangle is displayed around the face of a person not wearing a face mask.

<i>Code Credits and Inspiration:</i> Prajna Bhandary

<i>Prajna Bhandary Repo Link</i> <a href="https://github.com/prajnasb/observations.git">Link to Repo</a>
