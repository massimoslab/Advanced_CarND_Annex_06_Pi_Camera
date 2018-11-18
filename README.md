[image1]: ./images/picam_1.jpg
[image2]: ./images/picam_2.png
[image3]: ./images/picam_3.png

# Annex 06 : Raspberry Pi camera

For this project you need to purchase a four-wheel car chassis with rear wheel propulsion and front wheel steering mechanism.

Traditional four-wheel car chassis that you can find in the internet have a four-motor mechanism and steering is achieved by activating the two motors on either side of the car.

A car chassis with a front wheel steering mechanism allows you to steer the two front wheels like in a real car. By learning how t o use this car chassis you will be able to:

1. use all techniques that you will learn or have already learned in the CarND courses;
2. familiarize yourself with the mechanisms and issues that correspond to real-world problems.

The image below shows the car chassis as it is after assembly:

![alt text][image1]

The wheel system is well designed. There are two bearings on either side of the wheel that make the system very efficient and resistance free.

## 01. The motor

The motor is a 380 high-speed motor which can achieve significant speed. The rear mechanism consists of a differential mechanism mounted within a pre-assembled gear box. The biggest advantage of the differential mechanism is that when turning the internal wheel can have a different speed from the external wheel.

![alt text][image3]

The rear gear reduction mechanism that is extremely simple to mount. The motor and the gears are made of metal and they are very resistant. The issue I found with this car chassis is that it is a bit loud when running at full speed.

## 02. The servo

The servo is a MR996 servo system. The steering servo is attached to the front of the chassis through two L-shaped metal supports. The servo drives the steering angle of the front wheels through two adjustable bars, one of which connects both front wheels and the other connect to one of the two wheels.

![alt text][image5]

## 03. Car chassis assembly

Start by assembling the rear mechanism. Firstly fix the rear gear box to the metal base by using the appropriate screws. Ensure that no dirt or small debris do not enter the gear mechanism from the bottom. Once the mechanism has been fixed, connect the metal bar suspensions with the two rear bearings holders. Finally assemble the wheels and fix them with the appropriate bolts.

![alt text][image4]

As a second step, assemble the front steering mechanism. First of all fix the servo with the two provided L-shaped bars to the metal base as shown below without fixing the bar, which will be fixed later.

![alt text][image6]

Now, fix the bearing housing to the two front wheels and fix the wheel with the appropriate bolt.

![alt text][image2]

Once the two front wheel have been fixed to the bearing housing, you can connect them to the metal base as shown in the image below:

![alt text][image7]

Finally, you can connect the adjustable plastic-metal bars to one of the bearing housing.

![alt text][image8]

## 04. Python code

```
camera.start_preview()
sleep(5)
camera.capture('/home/pi/Desktop/image.jpg')
camera.stop_preview()
```

## 04. Purchases
The car chassis can be purchased on the internet. I have purchased mine from ebay:
[Purchase a car chassis here](https://store.arduino.cc/)

## Author

**Massimo Passamonti**: [email me](me@massimoslab.com)

## License

This project and its source code are licensed under the MIT License. [See MIT License](https://github.com/github/choosealicense.com/blob/gh-pages/LICENSE.md) file for more details.
