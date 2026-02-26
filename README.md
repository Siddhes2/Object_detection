Object Detection with YOLOv5 in Google Colab
This notebook demonstrates how to perform object detection using a pre-trained YOLOv5 model from Ultralytics within a Google Colab environment.

Project Description
This project leverages the powerful YOLOv5 (You Only Look Once, version 5) model for real-time object detection. The notebook shows a simple workflow:

Installation of the ultralytics library.
Loading a pre-trained yolov5s model from torch.hub.
Performing inference on an example image.
Displaying the detection results.
Setup and Installation
To run this notebook, you will need a Google Colab environment. The necessary dependencies can be installed using pip.

Prerequisites
Google Colab account.
An image file for testing (e.g., /content/istockphoto-1426458619-612x612.jpg as used in the example).
Installation Steps
Run the following command in a Colab code cell to install the ultralytics library:

!pip install ultralytics
How to Run
Open the .ipynb notebook file in Google Colab.
Ensure you have your test image uploaded to the Colab environment (e.g., /content/istockphoto-1426458619-612x612.jpg). You can upload files using the file browser on the left sidebar in Colab.
Run all cells in the notebook sequentially.
Code Snippets
Installation:

!pip install ultralytics
Object Detection:

import torch
from PIL import Image

# Load YOLOv5s model
model = torch.hub.load('ultralytics/yolov5', 'yolov5s')

# Load an image (make sure this path is correct for your uploaded image)
img = Image.open("/content/istockphoto-1426458619-612x612.jpg")

# Perform inference
result = model(img)

# Display results
result.show()
Expected Output
The result.show() command will display the input image with bounding boxes and labels for detected objects drawn on top of it. This will appear as an inline image in the Colab output.

