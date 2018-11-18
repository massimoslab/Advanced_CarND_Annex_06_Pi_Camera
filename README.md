[image1]: ./images/picam_1.jpg
[image2]: ./images/picam_2.png
[image3]: ./images/picam_3.png
[image4]: ./images/picam_4.jpg
[image5]: ./images/picam_5.jpg

# Annex 06 : Raspberry Pi camera

The Raspberry Pi camera is a an official product of the Raspberry Pi Foundation. There are two official version that you can purchase:
1. a 5-megapixel model released in 2013; and
2. an 8-megapixel model released in 2016.

Be careful when purchasing the picamera online as there are several replicas that can be found with much lower quality. Having said that there is a type of camera that is an unofficial camera but that has several advantages: a wide-angle lens, also called fish-eye lens.

For this project I have used two type of cameras. The first one is the official Raspberry 8-megapixel picamera, which will be used for high accuracy tasks:

![alt text][image4]

The second camera is a cheaper fish-eye camera, that will be used for lower accuracy tasks:

![alt text][image5]

## 01. Assembly

Start by making sure that the Raspberry Pi is switched off. Locate the camera connector slot (notice that there are two slots on the Raspberry Pi 3), open the connector by pulling slightly the plastic tab, insert the flat cable and push the plastic tab back to its original position. Once connected the camera will look like this:

![alt text][image1]

Switch on the Raspberry Pi and open the Raspberry Pi Configuration Tool from the main menu:

![alt text][image2]

Once in the Raspberry Pi Configuration Tool make sure that the camera software is enabled:

![alt text][image3]

## 02. Python code 1

Run the following python code to display on the raspberry pi screen the image captured by the picamera.

```
from picamera import PiCamera
from time import sleep

camera = PiCamera()

camera.start_preview()
sleep(10)
camera.stop_preview()
```

## 03. Python code 2

Run the following python code to take a picture with the picamera and save the image on the desktop with the name **image.jpg**.

```
camera.start_preview()
sleep(5)
camera.capture('/home/pi/Desktop/image.jpg')
camera.stop_preview()
```

## 04. Purchases
The official picamera can be purchased on the Raspberry Pi Foundation website:
[Purchase a picamera here](https://www.raspberrypi.org/products/camera-module-v2/)

## Author

**Massimo Passamonti**: [email me](me@massimoslab.com)

## License

This project and its source code are licensed under the MIT License. [See MIT License](https://github.com/github/choosealicense.com/blob/gh-pages/LICENSE.md) file for more details.
