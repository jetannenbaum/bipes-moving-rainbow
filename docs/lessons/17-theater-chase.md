# Theater Chase

![Chase Animation](../img/chase-animation.gif)![Chase Animation](../img/chase-animation.gif)

Theater [Chase](https://en.wikipedia.org/wiki/Chase_(lighting)) is a classic pattern that was popularized in [marquee](https://en.wikipedia.org/wiki/Marquee_(structure)) signs above movie theaters.  It consists of a row of lights that were usually switched on and off so it would appear that the lights were moving or being chased around the edge of the signs.

## Sample Theater Chase Function

To create the illusion of pixels moving along a strip, we need to have three nested loops:

1. The inner "i" loop just moves from 0 to the number of pixels in steps of 3 (or a similarly small number).  It turns every 3rd pixel on, waits and then turns it off
2. The middle "j" loop just offsets the starting point of the inner loop moving from values of 0, 1 and 2.  The index in the inner loop is ```i+j```.
3. The outer-most  loop just indicates how many times the pattern should be repeated

Here is a sample of the theater_chase function that has four parameters:

1. the color
2. the delay (about 50 milliseconds)
3. the number of times the pattern should be repeated (iterations)

![Theater Chase Blocks](../img/theaterChase.jpg)

If you want to lower the power of the LED strip, you can change the skip number in the inner loop from 3 to 4, 5 or 6 etc.

## Main set of Blocks

This set of blocks will run a theater chase for the seven colors of the rainbow and then repeat.

![Theater Chase Main Blocks](../img/theaterChaseMainBlocks.jpg)

## Exercises

1. Add the skip number as an additional parameter to the function
2. Add another parameter that reversed the direction of the movement
3. Create a function that randomly changes the direction every few seconds