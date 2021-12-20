## Welcome to LED Matrix

This is the documentation for creation of a 10x15 LED Matrix that can be used to show animations and play Tetris, the fabrication and design of the Matrix were done 
at Astra Robotics RVCE 

# Tutorial

## Building the matrix
### Parts Required
1. A 2 x 4 ft piece of 0.5 inch thick plywood
2. A 5V, 4A Power Supply (Even a 2A power supply would do)
3. An Arduino Board 
4. 150 Individually Addressable LED's (WS2812B)
5. Standard tools such as a drill, and a screwdriver

### Assembly
1. Drill 10 * 15 equally spaced holes within the matrix in order to fit your LED's through each of the holes
2.  Daisy Chain the LED's from top to down (they usually come in packs of 50 LED's)
3. Connect the 5V Power supply to the appropriate terminals of the LED strips (Note: there will be a voltage drop when moving from one set of 50 LED's to the next so it is suggested to give a parallel power supply connection to each set).
4. Flash the Arduino Board with the given code for either Tetris or Animations
5. Connect the input pin of the WS2812 LED's to the D3 Pin of the Arduino and the VIN and GND pins of the Arduino to the power supply.
6. It is recommended to use a white cloth or a diffusing sheet in order to view the matrix better

### Code
The code for the programs are given for different applications [here](https://github.com/Mnzs1701/LED_Matrix_Astra.git)
#### Tetris
This is to make a playable game using an Android Phone and the LED Matrix over Bluetooth
It requires an additional HC-05/HC-06 Bluetooth Module connected to the Matrix in order to function.
Download the APK and connect the Bluetooth Module to the matrix in order to play the game

#### Animations
The animations of a [beating heart](https://github.com/Mnzs1701/LED_Matrix_Astra/blob/master/Matrix_Heart_Beat.ino) and a [snowy christmas tree](https://github.com/Mnzs1701/LED_Matrix_Astra/blob/master/Matrix_TreeAnimation.ino) are given in the code 

### Results!
![snowy_christmas_tree](https://media.giphy.com/media/TVvYrRyzL71XlXJtQc/giphy.gif)

## Creating More Animations
Use the [Piskel App](https://www.piskelapp.com/) to create new animations

### Steps
1. Create a new drawing and edit the size of the drawing to be 10x15 pixels (Size of the matrix)
2. Use multiple frames in order to create your sprite sheet
3. When you are done, save the drawing and export it into the C format
4. Use the accompanying C++ Program to reverse the hex bits of the animation in order to display it on the matrix (the default color scheme is reversed)
5. Replace the frames in the Arduino Code with your custom animation
