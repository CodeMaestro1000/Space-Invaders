# Space-Invaders
An atari style space invader handheld game on the TM4C Microcontroller

# Preface
This project was developed using examples provided by Professor Jonathan Valvano in his book Real-Time Operating Systems for ARM Cortex-M Microcontrollers.

# Usage
To run the space invaders game, you'll need a Stellaris launchpad (can also work on any cortex M4 microcontroller) and a Booster pack. The booster
pack can be found [here](https://www.ti.com/tool/BOOSTXL-EDUMKII?keyMatch=Educational+BoosterPack&tisearch=Search-EN-Everything&ref_url=https%25253a%25252f%25252feducation.ti.com%25252fen%25252ffaculty%25252fteaching-materials-and-classroom-resources%25252fproducts-and-tools%25252fevaluation-modules)
and the lauchpad [here](https://www.ti.com/tool/EK-TM4C123GXL).
Simply build the entire project using the IDE of your choice (I used Keil uVision but with a bit of tweaking, you can get it to build on your
preferred one). The entrypoint of the program is the `main.c` file.

# Operating System
The source code for the RTOS can be found in `os.c` and `os.h` files. These files contain a series of functions for initiating the thread control block structure,
scheduling tasks, killing, sleeping etc.
The `osasm.s` file contains low-level commands implemented in assembly for starting the OS and using the SysTick Handler for context switching.

# Images
The `images.h` file contains 18x13 bitmap implementation for sprites. Sprites include the spaceship, monsters and obstacles.

# Sound
`Sound.c` contains several in-game sounds implemented using PWM techniques. Sounds play through the buzzer on the MKII board.

# Demo
Here's a video I recorded while playing the game:


https://github.com/CodeMaestro1000/Space-Invaders/assets/46170255/a689260c-7e3c-456f-96b9-ba53e0d261c0


