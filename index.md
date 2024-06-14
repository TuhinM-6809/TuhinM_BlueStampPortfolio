<!--//You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:-->

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Tuhin M | Bellarmine College Preparatory | Electrical Engineering and Computer Science | Rising Sophomore |

# Gesture Controlled Robot

<!--
**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 
-->
# First Milestone
Completed 6/14/24
<iframe width="560" height="315" src="https://www.youtube.com/embed/WIJjrf_RyUc?si=iWhdWPHIjlC2sGut" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

  My first milestone was purely mechanical and hardware based. I wanted to completely build all of the electrical and mechanical parts of the robot car. In order to accomplish this, I first attached four motors to a baseplate and wired them to the motor controller. Then, I connected the motor controller to the Arduino Uno and connected the battery pack to the Arduino Uno. Then, I connected all of the motor wires to teh Arduino Uno and the motor controller. Once I did that, I attached the wheels and fastened the top plate to the robot. 

  The technical side of what is happening within the robot is that the power from the battery pack travels to the Arduino Uno which provides power to the motor controller. Then, the motor controller provides power to the motors, enabling them to run. 
  
  Some challenges I faced was that the motors had some trouble providing enough torque to spin the wheels. I solved this problem by letting them warmup before I attached the wheels. Another problem I faced was that one of the motors wasn't spinning. After debugging for a while, I discovered that it was because the motor wires weren't soldered properly together. Once I fixed this, I ran some expiremental code to test whether the motors would spin and the all succesfully spun. 
  
  Going forward, I plan to complete all of the hardware for the gesture controller. Then, I want to run the code and test whether or not the car will move according to the gesture detection. Once I complete all of these steps and ensure that the robot is fully functional with the gesture controller, I plan to add some extra features like side to side movement.


# Schematics 

![Headstone Image](how_to_make_hand_gesture_control_robot_via_bluetooth_Idj2KLCd3B.png)

# Code

Test Code for Running Motors
```c++
//Test Code for Running Motors
int In1 = 7; //Defining Digital Pins for Motors
int In2 = 8;
int In3 = 4;
int In4 = 12;
int ENA = 5; //Defining ENA for both sides
int ENA2 = 6;
int SPEED = 210; //Defining the speed of the wheels

void setup()
{

pinMode(In1,OUTPUT); //Designating the motors as outputs
pinMode(In2,OUTPUT);
pinMode(In3,OUTPUT);
pinMode(In4,OUTPUT);
pinMode(ENA,OUTPUT);
pinMode(ENA2,OUTPUT);

digitalWrite(In1,HIGH); //Setting the motor direction, either HIGH or LOW
digitalWrite(In2,LOW);
digitalWrite(In3,HIGH);
digitalWrite(In4,LOW);

analogWrite(ENA,SPEED); //Setting the speed for both sides
analogWrite(ENA2,SPEED);

}

void loop()
{

}
```

# Bill of Materials

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino UNO | Used to control the robot movement | $25.81 | <a href="https://www.newark.com/arduino/a000066/dev-board-atmega328-arduino-uno/dp/78T1601?COM=ref_hackster&CMP=Hackster-NA-project-94b13d-Jun-24"> Link </a> |
| Arduino Nano R3 | Used for the hand mounted part | $23.23 | <a href="https://www.newark.com/arduino/a000005/dev-board-atmega328-arduino-nano/dp/13T9275?COM=ref_hackster&CMP=Hackster-NA-project-e1c9f9-Jun-24"> Link </a> |
| Inertial Measurement Unit (IMU) (6 deg of freedom) | Used for sensing changes and movement | $5.99 | <a href="https://www.amazon.com/dp/B008BOPN40/?tag=octopart00-20"> Link </a> |
| SparkFun Dual H-Bridge motor drivers L298 | Used to control the motors | $7.21 | <a href="https://www.amazon.com/Diymall-Module-Stepper-Modules-Arduino/dp/B00NJOTBOK/ref=asc_df_B00NJOTBOK/?tag=hyprod-20&linkCode=df0&hvadid=693611984328&hvpos=&hvnetw=g&hvrand=11587990999031796711&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9032183&hvtargid=pla-2062985254553&psc=1&mcid=170f1bbf2f773d04a1c0254ec6413a12&gad_source=1"> Link </a> |
| Solderless Breadboard Half Size | Used to hold the pins and devices for the controller | $4.96 | <a href="https://www.newark.com/adafruit/64/bread-board-prototype-electronics/dp/53W6131"> Link </a> |
| HC-05 Bluetooth Module | Used for connecting the robot car to the controller on the wrist | $10.39 | <a href="https://www.amazon.com/HiLetgo-Wireless-Bluetooth-Transceiver-Arduino/dp/B071YJG8DR"> Link </a> |
| Male/Male Jumper Wires | Used to connect electronics to the boards | $2.10 | <a href="https://www.digikey.com/en/products/detail/sparkfun-electronics/PRT-12795/5993860?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=Pmax_Shopping_Product_Silicon%20Valley%20Category%20Awareness&utm_term=&utm_content=&utm_id=go_cmp-20773039395_adg-_ad-__dev-c_ext-_prd-5993860_sig-CjwKCAjwjqWzBhAqEiwAQmtgT4yqEvNPG-CeiyWY2SfxfZpecU3iTeRpYc_iE8nQLuzfGLUG7xOabxoCPq8QAvD_BwE&gad_source=1&gclid=CjwKCAjwjqWzBhAqEiwAQmtgT4yqEvNPG-CeiyWY2SfxfZpecU3iTeRpYc_iE8nQLuzfGLUG7xOabxoCPq8QAvD_BwE"> Link </a> |
| Male/Female Jumper Wires | Used to connect electronics to the boards | $4.11 | <a href="https://www.newark.com/adafruit/826/wire-gauge-28awg/dp/88W2802?COM=ref_hackster"> Link </a> |
| DC Motor, 12 V | Used to make the robot move | $2.10 | <a href="https://www.digikey.com/en/products/detail/sparkfun-electronics/ROB-11696/6163657?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Low%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20243063506_adg-_ad-__dev-c_ext-_prd-6163657_sig-CjwKCAjwjqWzBhAqEiwAQmtgT6PUzEZcO3nk_kRwzXNGFYU7V3DIX_euwD9z8G3limBqyci_jx-AWxoC1YkQAvD_BwE&gad_source=1&gclid=CjwKCAjwjqWzBhAqEiwAQmtgT6PUzEZcO3nk_kRwzXNGFYU7V3DIX_euwD9z8G3limBqyci_jx-AWxoC1YkQAvD_BwE"> Link </a> |
| Pimoroni Maker Essentials - Micro-motors & Grippy Wheels | Used to translate the motor power to movement | $33.79 | <a href="https://shop.pimoroni.com/products/maker-essentials-micro-motors-grippy-wheels?variant=1418711662602"> Link </a> |
| Rocker Switch, SPST | Used to switch the robot and controller on and off | $1.26 | <a href="https://www.digikey.com/en/products/detail/triad-components-group,-inc/RF1-1A-DC-2-R-1/11492837?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Low%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20243063506_adg-_ad-__dev-c_ext-_prd-11492837_sig-CjwKCAjwjqWzBhAqEiwAQmtgT7oTJas8J3dyOTnXepZN0X2aoT77Lba8JHsMW7X9lC3OWGfcfXICZBoC4eEQAvD_BwE&gad_source=1&gclid=CjwKCAjwjqWzBhAqEiwAQmtgT7oTJas8J3dyOTnXepZN0X2aoT77Lba8JHsMW7X9lC3OWGfcfXICZBoC4eEQAvD_BwE"> Link </a> |
| 9V Battery Clip | Used to connect to the battery pack | $0.309 | <a href="https://www.newark.com/keystone/233/battery-strap-9v-wire-lead/dp/22C4351"> Link </a> |
| 9V battery (generic) | Used to power the robot | $1.54 | <a href="https://www.tequipment.net/Techni-Pro/TNP-AL9V-ea/Batteries-and-Chargers/?Source=googleshopping&gad_source=1&gclid=CjwKCAjwjqWzBhAqEiwAQmtgT4aHyiP0JiLkauY-n9bLEDgScQHZIqa6-ZshwL10lhdLS98RW5EJBBoC1nQQAvD_BwE"> Link </a> |
| Battery Holder, 18650 x 2 | Used to hold the batteries | $9.48 | <a href="https://www.newark.com/keystone/1048/battery-holder-18650-li-ion-2cell/dp/56T2029?COM=ref_hackster&CMP=Hackster-NA-project-94b13d-Jun-24"> Link </a> |
| Arduino IDE | Used to code the functionalities of the robot | $0.00 | <a href="https://www.arduino.cc/en/software"> Link </a> |


<!--# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.-->

# Arduino Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/MTDgItoHk8w?si=aqH-RLGaW8Hp8VCv" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

The Arduino Starter Project provided a basic foundation for learning soldering and coding with Arduino. As part of the project, I built a Proto Shield for the Arduino UNO. This Proto Shield featured a reset button, resistors, LEDs, and rails for wire inputs. Using the Proto Shield, the Arduino UNO, and breadboard I built a circuit with a LED that was controlled by a button. I coded this button and LED using Arduino IDE, an application that uploaded code to the Arduino UNO. I used conditional statements to detect button presses and translate the result gained into a signal to turn the LED on or off.

# Code

```c++
//Defining the LED position on the Breadboard
#define LED_PIN 8
//Defining the Button position on the Breadboard
#define BUTTON_PIN 7

void setup() {
  //Defining the LED as the Output
  pinMode(LED_PIN, OUTPUT);
  //Defining the Button as the Input
  pinMode(BUTTON_PIN, INPUT);
}
void loop() {
  if (digitalRead(BUTTON_PIN) == HIGH) { //If the button is pressed
    digitalWrite(LED_PIN, HIGH); //Turn on the LED
  }
  else { //If the button is not pressed
    digitalWrite(LED_PIN, LOW); //Keep the LED off
  }
}
```

# Bill of Materials

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino Uno | Control the circuit power and ground | $24.50 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| USB A -> B cable | Connection to computer | $9.89 | <a href="https://www.amazon.com/Amazon-Basics-External-Gold-Plated-Connectors/dp/B00NH13DV2?th=1"> Link </a> |
| Arduino Proto Shield | Used to make easier wire connections | $9.95 | <a href="https://learn.adafruit.com/adafruit-proto-shield-arduino"> Link </a> |
| Breadboard | Used to hold LED, Button, and wiring | $2.90 | <a href="https://www.digikey.com/en/products/detail/dfrobot/FIT0096/7597069?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_High%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20222717502_adg-_ad-__dev-c_ext-_prd-7597069_sig-CjwKCAjw65-zBhBkEiwAjrqRMI_n1aAgL784j99C-KhXqSOPK8ByCWra4Myz7QmtGApcpn9UfPkQYRoCAbgQAvD_BwE&gad_source=1&gclid=CjwKCAjw65-zBhBkEiwAjrqRMI_n1aAgL784j99C-KhXqSOPK8ByCWra4Myz7QmtGApcpn9UfPkQYRoCAbgQAvD_BwE"> Link </a> |
| Male to Male Connectors | Used to connect electronics | $2.10 | <a href="https://www.digikey.com/en/products/detail/sparkfun-electronics/PRT-12795/5993860?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=Pmax_Shopping_Product_Silicon%20Valley%20Category%20Awareness&utm_term=&utm_content=&utm_id=go_cmp-20773039395_adg-_ad-__dev-c_ext-_prd-5993860_sig-CjwKCAjwjqWzBhAqEiwAQmtgT6kuQk86BHPzUXokCss1tlPM5KsUHGUijRBNL3osiZAj6gI66WffEBoCMDIQAvD_BwE&gad_source=1&gclid=CjwKCAjwjqWzBhAqEiwAQmtgT6kuQk86BHPzUXokCss1tlPM5KsUHGUijRBNL3osiZAj6gI66WffEBoCMDIQAvD_BwE"> Link </a> |
