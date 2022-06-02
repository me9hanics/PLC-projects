University PLC project

![IMG_20220602_151656](https://user-images.githubusercontent.com/82604073/171654840-97526c9c-853d-4bd6-93bd-290efcf3eace.jpg)


Firstly (after reset), the conveyer belt moves to the "right". If an object is detected by a sensor, then the conveyer belt stops, and it can be starting again by pressing the correct button. If we reach the farthest sensor, then the conveyer belt stops for 3 seconds, then it switches conveying directions.

The model was designed to keep hold of multiple objects. If multiple sensors detect an object, it is only possible to start the conveyer belt again if all buttons corresponding to the sensors which detected an object are pressed.
The sensor is not capable of outputting a constant high logic level voltage, thus it's output "bounces". For this, I had to "debounce" the sensor in the software, I added a 0.7 second minimum time limit to switch states after getting in a "go" state.

I designed the model using state machine logic, and with ladder diagrams.

![plc](https://user-images.githubusercontent.com/82604073/171645403-c268f15b-cf24-4dab-ae28-ed2d3aface52.png)
