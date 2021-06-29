# face-mask-detection
A system that detects whether a person is wearing a face mask or not.

The system uses MobileNetV2 architecture, which is a pre-trained CNN model consisting of 53 layers trained on ImageNet dataset, as the backend framework.

The deep learning model is trained on images with labels as 'with_mask' and 'without_mask', 'with_mask' class consisting of 4150 images and 'without_mask' class consisting of 4195 images. The model is then saved onto disk and loaded during the detection phase.

The detection is done over the live video stream using OpenCV library, first extracting the Region of Interest, and then performing mask detection using the deployed model.

The person wearing a face mask is indicated by a green rectangle around the face of that person, while a red rectangle is displayed around the face of a person not wearing a face mask.

The system can be initialized by executing the detect_mask_video.py script, which will use the camera available on the machine executing the script.

<i>Code Credits and Inspiration:</i> Prajna Bhandary

<i>Prajna Bhandary Repo Link</i> <a href="https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqblY0NTd5UkVJbll0OWpXMXRFZW1leG5kRVFQUXxBQ3Jtc0tuS21WQUtkdUxqTEp2WS1QMWljZWlfYmVaMHVQVy1PYmhXVDJEdEtZY1dCZ2lJY0dtM2FpeC02dkVUcjVtN0lNbHZSN21uYXU4TDdpX1RvQUdYOHhTTVAyM0xoRVV2c2h4Zk9jTmsxd09pc0VyWmZkaw&q=https%3A%2F%2Fgithub.com%2Fpik1989%2FFaceMaskDetection">Link to Repo</a>
