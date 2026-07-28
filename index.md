# Mechanical Hexapod
I built a mechanical hexapod, capable of movement through a remote control. 18 motors provide 3 different points of rotation on each leg. All the motors are wired into a central PCB, which coordinates the movement of the legs. Throughout this project I learned about soldering techniques, taking apart pre-made components, and the importance of clean wiring. The robot uses the freenove hexapod robot library in order to control movement, and is wirelessly controlled from a custom app.

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
// this is only the code that i added onto the premade processing code

// orange colors
int princetonorange = color(231, 117, 0);
int darkerprincetonorange = color(225, 110, 10);
int neonorange = color(255, 128, 0);
int Hoverorange = color (275, 148, 20);
int activeorange = color (235,88,10);
// variable for the leg number
int leg = 1;
//variable for toggle switch
int Switch;

void setup() {
  //custom on/off switch
  cp5.addSlider("On/Off")
  .setRange(0,1)
  .setSize(50,100)
  .setPosition(15,450)
  .setNumberOfTickMarks(2)  
  .setSliderMode(Slider.FLEXIBLE)  
  .moveTo("Custom")
  .setId(505)
  ;
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
| Freenove Hexapod kit with remote | Stock Hexapod kit that is built off of | $126.99 | <a href="https://store.freenove.com/products/fnk0031?_pos=2&_sid=7d0b7bccf&_ss=r"> Link </a>|
| ESP32 cam | Small camera that can wirelessly connect with your phone | $16.99 | <a href="https://www.amazon.com/Hosyond-ESP32-CAM-Bluetooth-Development-Compatible/dp/B09TB1GJ7P/ref=sr_1_1_sspa?crid=1PYWP76XEPUX1&dib=eyJ2IjoiMSJ9.LTQ8QA0yrlsQjvOEHKz0wYVcZ5xnBzG8J5dNZ0DD9vKq1cCzINpkS8IK2knuAhaAkXTJEC6CuOPqw4R1QAn2luihWUnIICA-bIO3Iw7MfKqCC8pPc6BqRKLmo_J7c_ZKxDKDZCA86pU8x788mZ7AXVHf7Osr_5yzdPCB4PIcf158O0hzXKHuRSMbnzXInDmAwAwpnnBLzRQXdY939j2M7ukqfmpk93_Bxv4JAAg9VXwNojZsd1QO5e2lB5rUCu7z1ASxnYAUpdVDKSLmoKhmAOXAqkV-FdDaTyKpWLuClOk.MyZEHK4I4-_fnt4eEQd_lkuSMOWcgSMUHEjRvKCXKaQ&dib_tag=se&keywords=esp%2B32%2Bcam&qid=1785256377&s=electronics&sprefix=esp32%2Bca%2Celectronics%2C168&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1"> Link </a> |
| Jumper Wires | Connecting the ESP32 camera | $6.98 | <a href="https://www.amazon.com/Elegoo-EL-CP-004-Multicolored-Breadboard-arduino/dp/B01EV70C78/ref=sr_1_1_sspa?dib=eyJ2IjoiMSJ9.I3nSspk5onl8Jong0G-0EaUV8k3yvkfNxu9EofYJ660j1dYXWvGcCaWvoPmVbWbzzPiX0Bw5dl8Pr07K6QkBVPexY0UkSW47Q9SO-dMAQWC6JT9dpAdBsD8kVqvTtErn9OF2LiurxqcDtFwg-ay6NkZJM15E7_IyUAeFj7qvU6ivMWRnEa7Oywa5bZ8qSMR3FyAS9aprB5wY9XOAQxd5djTF0tjEsvM_i2-lskb2Elg.Xg2TyKcgDpGMPq1DHWtwH_LbrA0mJIhB56GoVMBputg&dib_tag=se&keywords=jumper%2Bwires&qid=1785256526&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1"> Link </a> |
| Tenergy 7.2v battery | Rechargeable battery  | $39.49 | <a href="https://power.tenergy.com/tenergy-nimh-7-2v-3800mah-battery-pack-w-tamiya-connector-for-rc-cars/?sku=11200&gad_source=1&gad_campaignid=17180860516&gbraid=0AAAAAD_fnYHNIx6mPo78v9NZtPMzOhEb3&gclid=CjwKCAjwpqHTBhAcEiwAj2Afunb-jK0Ndfn2y9CvKmIICochYAEYZYYaSSELZy5lhx8zllzCMItN4BoCr98QAvD_BwE"> Link </a> |
| Tenergy 7.2v battery connector | Connecting the battery to the hexapod | $Price | <a href="https://power.tenergy.com/standard-female-tamiya-connector-charger-side/?sku=80000-4&gad_source=1&gad_campaignid=17180860516&gbraid=0AAAAAD_fnYHNIx6mPo78v9NZtPMzOhEb3&gclid=CjwKCAjwpqHTBhAcEiwAj2AfugP0WQJD69mX2IXxH-gn-QoSnGoiYZ7LDq-sQmniZ23Bs8OhSqcT5BoCx8kQAvD_BwE"> Link </a> |


