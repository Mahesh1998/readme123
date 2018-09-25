# INTRODUCTION:

The TensorFlow Object Detection API is an open source framework built on top of TensorFlow that makes it easy to construct, train and deploy object detection models.

## Method & Model:

### SSD: [Single Shot Multi Box Detector]

SSD is an unified framework for object detection with a single network. You can use the code to train/evaluate a network for object detection task. SSD is used for detecting objects in images using a single deep neural network. Our approach, named SSD, discretizes the output space of bounding boxes into a set of default boxes over different aspect ratios and scales per feature map location. At prediction time, the network generates scores for the presence of each object category in each default box and produces adjustments to the box to better match the object shape. Additionally, the network combines predictions from multiple feature maps with different resolutions to naturally handle objects of various sizes. Our SSD model is simple relative to methods that require object proposals because it completely eliminates proposal generation and subsequent pixel or feature resampling stage and encapsulates all computation in a single network. This makes SSD easy to train and straightforward to integrate into systems that require a detection component. Experimental results on the PASCAL VOC, MS COCO, and ILSVRC datasets confirm that SSD has comparable accuracy to methods that utilize an additional object proposal step and is much faster, while providing a unified framework for both training and inference. Compared to other single stage methods, SSD has much better accuracy, even with a smaller input image size. For 300×300 input, SSD achieves 72.1% mAP(mean average precision) on VOC2007 test at 58 FPS on a Nvidia Titan X and for 500×500 input, SSD achieves 75.1% mAP, outperforming a comparable state of the art Faster R-CNN model.


# INPUT:

A Video Feed(Recorded).


# OUTPUT:

Output would be a corresponding result with various detected objects surrounded by boxes with the labels and probability percentages.


# Installation and Procedure

## Requirements:

Tensorflow Object Detection API depends on the following libraries:<br>
<ul>
	<li>Tensorflow CPU Version</li>
    <li>Numpy</li>
	<li>Open CV</li>
	<li>Tarfile</li>
	<li>Matplotlib</li>
	<li>Pillow</li>
	<li>Matplotlib</li>
</ul>

## Steps:

<ol>
<li>Open the object_detection folder and search for object_detection_video.py (For Recorded Videos).</li>
<li>Open the file and find if __name__ == “__main__” (basically present at the bottom). There in give the path of the video over which you want to run, to detect objects.</li>
<li>Now, after specifying the path simply run the object_detection_video.py in order to start the object detection.</li>
<li>Output video would be saved in the static folder.</li>
</ol>


