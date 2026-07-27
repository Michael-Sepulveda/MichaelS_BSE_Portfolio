# Mechanical Hexapod
I built a mechanical hexapod, capable of movement through a remote control. 18 motors provide 3 different points of rotation on each leg. All the motors are wired into a central PCB, which coordinates the movement of the legs. Throughout this project I learned about soldering techniques, taking apart pre-made components, and the importance of clean wiring.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Michael S | Nueva | Mechanical Engineering | Incoming Sophmore

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone


<iframe width="560" height="315" src="https://www.youtube.com/embed/AGoMOEGSwcM?si=dOLVRxDzffaKcGPC" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My final milestone added modifications to the freenove hexapod. I went back to the calibration app in order to add custom controls the robot, and have buttons for custom movements. In order to make these modifications, I had to code and test the movements in arduino ide first. I then translated the code into java, so that I could add it to the processing app, which then creates the separate calibration app. Using the controlP5 library, I was able to add buttons and a custom tab for my code. The buttons call the commands that I made prior, and send those commands to the hexapod, which starts the movement that I coded. The buttons make the robot rock back and forth, bounce up and down, move it's body in a circle, and life it's legs in a wave like pattern. My final modification was connecting an esp32 camera to the hexapod's control board, which gives me wireless connection to a camera from my phone. The esp32 module plugs into the leftover pin slots on the board, which allows me to use the camera with the robot. The esp32 camera requires wifi, though, meaning I can't use the hexapod's wifi to control it. This means I needed 2 devices in order to have both movement and vision, hence the use of my phone. I printed out a simple holder for the camera, that would also fully secure the battery, but it was not printed at the time of recording the third milestone.


# Second Milestone


<iframe width="560" height="315" src="https://www.youtube.com/embed/oXx-ISeFiCc?si=HgS1ziBTH3oohgaX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My second milestone was the fully complete the stock hexapod. Since I was able to get motion and wireless connection in my first milestone, my next step was the get the hexapod working with the remote control. The remote control was also part of the kit, so I was able to follow to provided tutorial. However, like the tutorial for the robot, the video guide didn't mention the necessary arduino code prior to assembly. Luckily, I had run into the same issue when putting together the hexapod, so I knew to go onto the freenove website to look for the source code for the controller. I also downloaded the schematics for both the hexapod and controller, in preparation for future modifications. The controller uses a nrf24l01 module in order to communicate with the hexapod. I also got a simple battery casing 3d printed, just to keep the battery from possibly disconnecting during movement.
# First Milestone


<iframe width="560" height="315" src="https://www.youtube.com/embed/2KsnWkth43s?si=X-QJwAFgri54d0XL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My first milestone was getting the hexapod fully built. Using the online guides for the hexapod, I was to fully build the body of the hexapod. The guides also helped me fix the leg angles of the hexapod, allowing it to properly walk. While building, I desoldered the battery casing from the original board, as I needed to replace it with a separate, rechargeable battery. Desoldering the original board was super challenging, since I couldn't get the solder off with the desoldering tube. I also needed the soldering iron to get super hot, which made the whole process really dangerous. After prying off the original casing with a screwdriver, I was able to resolder new wiring on onto the positive and negative sides of the hexapod, and attach the connecter for the new battery. I followed the freenove instructions to use the hexapod's wifi in order to connect it to my computer. After connecting my computer, I used the built in calibration app in order to get the hexapod to move wirelessly. 

# Starter Project


<iframe width="560" height="315" src="https://www.youtube.com/embed/4rXpKrqahzc?si=QRLTm9MgB0hddihh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My starter project was the RGB slider. It consisted of 3 sliders, an led, usb port, and central board. All the componenets were soldered onto the board, and worked immediatly after soldering. When trying to show the slider working on camera though, it didn't work at first. We thought that maybe the wires were off, so we tried the one I used. That didn't work, so I resoldered the componenets, just incase I hadn't put enough solder the first time. That didn't fix the issue, though, so I had to plug the device into my computer. Thankfully, this powered the RGB slider with no issues. I'm still not sure why only my computer powers the rgb slider, but I'm glad that this was a one time issue.

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

