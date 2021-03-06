# Attribute-detection PoC 
Python code for detecting specified attributes of a person for a surveillance system proof-of-concept. This prototype uses a convolution neural network to detect specified attributes of a person. Based on the positive detection value, the camera will move and zoom-in on target using onvif.<br>

** CNN model and related information not uploaded **

## How this code work
This code continuously pull images from a real-time streaming camera, and detects a person in an image.  If a person has been detected, the code will create a csv with the person's location (top-right coordinate and bottom-left coordinate of bouding box)and input this csv and raw image into a trained CNN.  The CNN outputs a csv with the probabilities for negative and positive detections.  If a positive detection value is over 0.7, a script to move and zoom-in the camera via onvif is called.

References/called code: <br>
[Haarcascade source files](https://github.com/Itseez/opencv/tree/master/data/haarcascades)<br>
[ONVIF Java](https://github.com/milg0/onvif-java-lib)

## Input:<br>
![alt tag](https://github.com/kphongagsorn/human-detection-scripts/blob/master/images/input.jpg)<br>
## Output:<br>
![alt tag](https://github.com/kphongagsorn/human-detection-scripts/blob/master/images/output.jpg)<br>
Key:<br>
negative detection, positive detection


