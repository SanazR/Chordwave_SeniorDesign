# Chordwave


## What is ChordWave?

C﻿hordWave is an electronic musical instrument that produces sound using MIDI signals. The device is intended to be accessible and simple to use for individuals of any age and musical background.


![image alt](https://github.com/SanazR/Chordwave_SeniorDesign/blob/main/ChordWave-master/assets/CW.png?raw=true)


## Background

The ChordWave project intends to meet the rising need for contemporary and electronic musical instruments that offer a unique and unrestricted playing experience. Aspiring musicians may find it difficult to learn how to play traditional instruments since they can take many years of practice to perfect. A broader variety of tunes and capabilities are also required in instruments, enabling players to experiment with new musical styles and genres.  The ChordWave instrument aims to close this gap by providing a cutting-edge, digital alternative that is simple to use and has countless opportunities for enhancements.


![image alt](https://github.com/SanazR/Chordwave_SeniorDesign/blob/main/ChordWave-master/assets/image%20(1).png?raw=true)


## Problem Definition

The shortage of affordable and adaptable musical instruments that are suitable for both beginning and advanced performers in the digital era is the formal issue addressed by the ChordWave project. Beginners may find it difficult to learn existing instruments since they frequently demand complicated methods or an understanding of music theory. Additionally, a lot of instruments don't support trying out new and creative musical genres and have a limited sound palette. The ChordWave project aims to address these issues by developing a cutting-edge, digital musical instrument that is simple to use, adaptable, and promotes musical innovation.


## Objectives

The main goal of the project is to develop a digital musical instrument with limitless potential for updates and enhancements that enables users to quickly construct complicated chord progressions and melodies. The musical instrument should be simple to use and offer quick feedback along with a wide range of tones and effects. The following are key features of the ChordWave instrument:

- Easy-to-use interface
- Versatility
- Interconnectivity
- Durability and portability
- Cost-effectiveness


## Industry Standards

The ChordWave instrument's construction blends commercially available electrical parts with specially developed software to produce a distinctive musical experience. 

- #### MIDI Standards:
MIDI (Musical Instrument Digital Interface) is a standard for exchanging musical data among digital musical instruments, computers, and associated devices. To facilitate connection with other MIDI devices, including keyboards, sequencers, and computers, the ChordWave instrument embraces MIDI standards.

- #### BLE Communication Standards:
The wireless communication method used by the ChordWave instrument is MIDI over BLE (Bluetooth Low Energy). This standard enables the instrument to seamlessly and reliably transmit MIDI data to compatible devices, like computers, mobile phones, and tablets running music apps.

- #### I2C Internal Communication Standards:
Using the I2C (Inter-Integrated Circuit) Standard, the ChordWave instrument communicates internally amongst its parts. This standard makes it easier for a microcontroller, LCD, and other peripherals to exchange data for reliable and effective communication.



## Architecture Overview

The ChordWave instrument's construction blends commercially available electrical parts with specially developed software to produce a distinctive musical experience. Using 3D design tools, our team created the components, such as the wooden case and Plexiglass top, as well as the base PCB. The Iliauni FabLab then produced these designs utilizing laser cutting methods.

Writing code for the various parts and modules that are used as well as building firmware for the microcontroller are all included in the software development process. To ensure flawless integration and efficient use of the instrument, our team wrote and optimized the original software.

The ChordWave's physical design features a hardwood body with a Plexiglass top, providing a modern and aesthetically pleasing look. Musicians of different backgrounds and ability levels may readily interact with the instrument due to the instrument's emphasis on user-friendliness and easy controls.


## High-Level Overview

The fundamental operating component of the ChordWave instrument is an ESP32 microprocessor. Two GPIO extenders and an LCD display are connected to the ESP32 using the I2C protocol. One of the GPIO extenders is linked to a button matrix, while the other extender is linked to an RGB matrix, creating a 4x4 RGB button matrix pad. RGB matrix uses 16  pins of one extender, while the button matrix only uses 8 pins of another.

The ESP32 scans the user input from the button's matrix, analyzes them, and finds the right chords. Then, utilizing the MIDI over BLE (Bluetooth Low Energy) protocol, it transmits MIDI signals of the chord over Bluetooth. The ESP32 simultaneously produces feedback via the RGB matrix and the LCD display, improving the user interface and feedback.


## Detailed Design Description

The ESP32 microcontroller serves as the core operating unit of the ChordWave instrument. This robust microcontroller with a 32-bit dual-core CPU, offers the computing capacity required for scanning user inputs, processing data, producing MIDI signals, and managing the instrument's different components. The ESP32 has the benefit of having two distinct cores, which lets one core handle scan and processing functions while the second core handles output for low latency.

The ChordWave instrument has a button matrix attached to one of the GPIO extenders to ease user input. 12 note and 4 scale pads are grouped in a 4x4 structure in this button matrix. The button matrix can be easily connected to the ESP32 through the GPIO extender, which increases the number of available pins and is connected via the I2C protocol.

The instrument includes an RGB matrix in addition to the button matrix to give the user visual feedback. 16 individually controllable RGB LEDs are grouped in a 4x4 format in this RGB matrix, which is connected to the second GPIO extension. The ESP32 can individually operate each LED due to the GPIO extension, providing dynamic and programmable visual feedback.
The ESP32 and LCD display of the ChordWave instrument are linked via the I2C interface. The user can see information such as chord names, settings, and other relevant data on this display in real time. At address 0x3c, the ESP32 communicates with the LCD screen.

The I2C protocol is also used to provide interaction between the ESP32 and the GPIO extenders. The microcontroller and the extenders can transport data reliably and effectively due to this protocol. Addresses 0x3e and 0x3f are given to the GPIO extenders, respectively.

The instrument uses the MIDI over BLE (Bluetooth Low Energy) protocol for wireless communication. This standard enables the instrument to easily and reliably transmit MIDI data to suitable devices, such as mobile phones and tablets running music apps. 


## Analysis Result

- Latency of less than 15 milliseconds
- Low Power Consumption
- 10hr of Playtime
- Durable and robust


## Future Plans and Updates

- Add Synthesizer functionality
- Add MIDI Companion - AI that will play along with you
- Musical Workstation with a Looper and a Sequencer


## Team Members

- Temur Chichua
- Phidan Makhmudova
- Sanaz Rahbari 
  
## Attachements

You can watch the videos and check the photos of the instrument here

