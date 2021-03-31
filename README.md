# pi-altair-duino
Calculate pi on Altair-Duino
(https://github.com/ukupau/pi-altair-duino)

## Description
This was primarily an excercise for doing multi-byte division in assembly.

Simple pi calculation using the [Leibniz formula](https://en.wikipedia.org/wiki/Leibniz_formula_for_%CF%80)  
This series is known to converge quite slowly, but is relatively simple to implement, requiring just addition, subtraction and division.

Since the basic series calculates pi/4, all terms are multiplied by 4,000,000,0000.
So the result is pi * 1,000,000,000.

Calculates about 60 terms per second. Or roughly 250,000 per hour.

The number of terms to calculate is a 4 byte value (Note: it counts up to zero, not down). Calculating the the max 4 billion terms will take about 2 years.  
The upper 8 bits of the front panel address LEDs are used to show the progress. It will increment every 256 terms. The INTE LED is used to indicate when the last 64K terms are being calculated.

## Assembling
This project was tested on an Altair-Duino replica and not a real Altair.
Although I believe it should work.

Assembly and compilation was done using asm80.com. 

It should be loaded at address 0 to avoid interfering with the upper 8 address bit LEDs.

## Authors

* [Steven Chock](https://github.com/ukupau)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Links

* [asm80](https://www.asm80.com/) online assembler
* Altair-Duino [kit](https://adwaterandstir.com/altair/)
