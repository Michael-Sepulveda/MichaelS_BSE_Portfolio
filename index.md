# Mechanical Hexapod
I built a mechanical hexapod, capable of movement through a remote control. 18 motors provide 3 different points of rotation on each leg. All the motors are wired into a central PCB, which coordinates the movement of the legs. Throughout this project I learned about soldering techniques, taking apart pre-made components, and the importance of clean wiring.

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Michael S | Nueva | Mechanical Engineering | Incoming Sophmore

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/AGoMOEGSwcM?si=dOLVRxDzffaKcGPC" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My final milestone added modifications to the freenove hexapod. I took a step back and customized the calibration app in order to control the robot, and have buttons for custom movements. I made the robot rock back and forth, bounce up and down, move it's body in a circle, and life it's legs in a wave like pattern. I also was able to connect a esp32 camera to the hexapod's control board, which gives me wireless connection to a camera from my phone. I printed out a holder for the camera, that would also fully secure the battery, but it was not printed at the time of recording the third milestone.


# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/oXx-ISeFiCc?si=HgS1ziBTH3oohgaX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My second milestone was the fully complete the hexapod. Since I was able to get motion and wireless connection in my first milestone, my next step was the get the hexapod working with the remote control. The controller was used a nrf24l01 module in order to communicate with the hexapod. I also got a simple battery casing 3d printed, just to keep the battery from possibly disconnecting during movement.
# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/2KsnWkth43s?si=X-QJwAFgri54d0XL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My first milestone was getting the hexapod fully built. I followed the freenove instructions to get the hexapod connected to my computer through wifi, and used the built in calibration app in order to get the hexapod to wirelessly move. The battery casing had to be desoldered from the original board, as I needed to replace it with a separate, rechargeable battery.

# Starter Project

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

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

