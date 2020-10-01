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
  <img width="500" height="" src=images/cameraoptions.jpg>
</p>

The camera module OpenMV Cam H7 has a global shutter module that costs around 45 EUR.
Even though global shutter cameras are useful in some microfluidic applications, they are less available and have higher prices. More economical options exist such as the Sony 811 700TVL. However, instead of USB interface, these cameras have Analog High Definition (AHD) interface. The Raspberry Pi Camera Module V2 has interesting specs and a relatively low price; however the connection not being USB is a major disadvantage. The connection is made specifically for the Raspberry Pi through flat cable, which is not convenient for connecting and disconnecting regularly. Other camera modules exist, such as the Arducam B0203 that connect through USB; however they tend to be expensive.
For my requirements I chose the PlayStationEye camera for four main reasons: availability, cost, performance and connectivity. The main disadvantage is that additional drivers (CLEYE drivers and SDK) are required for the PS Eye to work on Windows, as well as for Mac OS (Operative System).

### PSEye 



## Light

## Structure

The structure consists mostly of 5mm laser cut acrylic, bars and collets. 

## Bill of materials 
