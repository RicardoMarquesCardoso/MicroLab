# Microscope

The microscope consists basically of a camera to acquire images, a circuit for lighting and a structure to allow holding and focusing of the sample.

<p align="center">
  <img width="500" height="" src=images/microscope.jpg>
</p>

The microscope was built using laser cutting techniques. 


## Camera

### Choosing a camera 

Based on previous studied open-source solutions, three main alternatives to a commercial microscope were identified: a USB microscope, a camera module or an altered webcam.
A few options were considered:


<p align="center">
  <img width="" height="" src=images/cameraoptions.PNG>
</p>

The camera module OpenMV Cam H7 has a global shutter module that costs around 45 EUR.
Even though global shutter cameras are useful in some microfluidic applications, they are less available and have higher prices. More economical options exist such as the Sony 811 700TVL. However, instead of USB interface, these cameras have Analog High Definition (AHD) interface. The Raspberry Pi Camera Module V2 has interesting specs and a relatively low price; however the connection not being USB is a major disadvantage. The connection is made specifically for the Raspberry Pi through flat cable, which is not convenient for connecting and disconnecting regularly. Other camera modules exist, such as the Arducam B0203 that connect through USB; however they tend to be expensive.
For my requirements I chose the PlayStationEye camera for four main reasons: availability, cost, performance and connectivity. The main disadvantage is that additional drivers (CLEYE drivers and SDK) are required for the PS Eye to work on Windows, as well as for Mac OS (Operative System).

### PSEye 

The PSEye fullfills all the requirements while being cheap and widely available. To transform this webcam into a microscope we need to simply invert the lens, going from concave to convex. An example on how to easily do this is found in [Hacketeria](https://www.hackteria.org/projects/ps3-eye-diy-microscopy-hack/). 

Two variables are essential for any basic microscope, focusing and zooming. Focusing is regulated by the distance between the lens and the sample, zooming by the distance between the lens and the CMOS. To allow for zooming, I designed a 3D printed part that allows the user to change the distance of the lens to the CMOS ([Part1](https://github.com/RicardoMarquesCardoso/MicroLab/blob/main/Microscope/Parts/%5BPSeye%5D%201.SLDPRT);[Part2](https://github.com/RicardoMarquesCardoso/MicroLab/blob/main/Microscope/Parts/%5BPSeye%5D%202.SLDPRT)). 

## Light

An independent circuit is responsible for illumination. One of the requirements for this microscope was that it should produce quality images even in total darkness. As so, a high-power LED was incorporated into the device. 

<p align="center">
  <img width="500" height="" src=images/lightscheme.PNG>
</p>

This circuit allows the microscope to be powered by a common powerbank, avoiding the need for another electrical outlet and making the microscope portable.

<p align="center">
  <img width="500" height="" src=images/microscopedark.jpg>
</p>


## Structure

The structure consists mostly of 5mm laser cut acrylic, bars and collets. 

## Bill of materials 

<p align="center">
  <img width="" height="" src=images/microscopebill.PNG>
</p>
