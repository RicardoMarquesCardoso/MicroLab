# Microscope

### Introduction

This describes a portable, low-cost, easy to build microscope suitable for the operation of microfluidic devices. 
The microscope consists of three main parts: 

* [Camera](#camera)
* [Light](#light)
* [Structure](#structure)

<p align="center">
  <img width="500" height="" src=images/microscope.jpg>
</p>

### Materials and tools

Besides all required [materials](#bill-of-materials), to replicate this project you will need access to a: 

* Laser Cutter machine;
* 3D printing machine; 
* Welding machine;

### About

This project was developed at the International Iberian Nanotechnology Laboratory by Ricardo Cardoso and supervised by Miguel Xavier,Ph.D. and researcher at INL. 
The main inspiration for this project was the [DropletKitchen's solution](https://dropletkitchen.github.io/index.html). Please go and review their project as a lot of information is complementary to this one!

## Camera

Shows you how to choose a suitable camera and how to alter it.

You will need some basic tools to take apart the camera and acess to a **3D printer**.

### Choosing a camera 

Based on previous studied open-source solutions, three main alternatives to a commercial microscope were identified: a USB microscope, a camera module or an altered webcam.
A few options were considered:


<p align="center">
  <img width="" height="" src=images/cameraoptions.PNG>
</p>

The camera module OpenMV Cam H7 has a global shutter module that costs around 45 EUR.
Even though global shutter cameras are useful in some microfluidic applications, they are less available and have higher prices. More economical options exist such as the Sony 811 700TVL. However, instead of USB interface, these cameras have Analog High Definition (AHD) interface. The Raspberry Pi Camera Module V2 has interesting specs and a relatively low price; however the connection not being USB is a major disadvantage. The connection is made specifically for the Raspberry Pi through flat cable, which is not convenient for connecting and disconnecting regularly. Other camera modules exist, such as the Arducam B0203 that connect through USB; however they tend to be expensive.
For my requirements I chose the PlayStationEye camera for four main reasons: availability, cost, performance and connectivity. The main disadvantage is that additional drivers (CLEYE drivers and SDK) are required for the PS Eye to work on Windows, as well as for Mac OS.

### PSEye  

The PSEye fullfills all the requirements while being cheap and widely available. To transform this webcam into a microscope we need to simply invert the lens, going from concave to convex. An example on how to easily do this is found in [Hacketeria](https://www.hackteria.org/projects/ps3-eye-diy-microscopy-hack/). 

Two variables are essential for any basic microscope, focusing and zooming. Focusing is regulated by the distance between the lens and the sample, zooming by the distance between the lens and the CMOS. To allow for zooming, I designed a 3D printed part that allows the user to change the distance of the lens to the CMOS ([Part1](https://github.com/RicardoMarquesCardoso/MicroLab/blob/main/Microscope/Parts/%5BPSeye%5D%201.SLDPRT);[Part2](https://github.com/RicardoMarquesCardoso/MicroLab/blob/main/Microscope/Parts/%5BPSeye%5D%202.SLDPRT)). 

**Missing pic of finished part**

## Light

An independent circuit is responsible for illumination. One of the requirements for this microscope was that it should produce quality images even in total darkness. As so, a high-power LED was incorporated into the device. 

You will need:

* [LED](https://pt.farnell.com/opulent/rebel-star-nw100/led-luxeon-rebel-star-nw100/dp/2115404);
* [LED Driver](https://www.digikey.pt/product-detail/en/recom-power/RCD-24-0.70-W/945-1125-ND/2256305);
* [Potentiometer (10kOhm)](https://www.amazon.com/Slide-Potentiometer-Single-Linear-Taper/dp/B00L9YDRU6);
* Wires;
* Welding machine;
* Male USB connector;

The circuit is very simple and it should take less than an hour to build. I advise you to check if the circuit is working (without welding) before mounting it onto the microscope structure. 

<p align="center">
  <img width="500" height="" src=images/lightscheme.PNG>
</p>

To simplify the powering of the circuit, a male USB connector is added to the end of the circuit. This allows the microscope to be powered by a common powerbank, avoiding the need for another electrical outlet and making the microscope portable.

<p align="center">
  <img width="500" height="" src=images/microscopedark.jpg>
</p>

**Missing pic of finished part**

## Structure

You will need:

* 1x A3 Acrylic sheets (5mm);
* 4x Steel Bar 6x70 mm;
* 2x Steel Bar 6x130 mm;
* 30x Collets 6mm;
* Laser Cutter;

Before cutting any piece in acrylic [check](https://github.com/RicardoMarquesCardoso/MicroLab/tree/main/Microscope/Parts) the measurements and test them with your machine setup. 

If it's the first time building the device I would suggest to print each part separately. 

### Step 1

<p align="center">
  <img width="" height="" src=images/Step2.1.PNG>
</p>

<p align="center">
  <img width="" height="" src=images/Step2.2.PNG>
</p>


### Step 2

<p align="center">
  <img width="" height="" src=images/camera2.PNG>
</p>

<p align="center">
  <img width="" height="" src=images/Step4.1.PNG>
</p>

### Step 3

<p align="center">
  <img width="" height="" src=images/step5.1.PNG>
</p>

## Bill of materials 

<p align="center">
  <img width="" height="" src=images/microscopebill.PNG>
</p>
