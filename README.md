Lab 4: Decimal/Hexadecimal number converter

This program is described in Chapter 5 of the Britton Textbook. Please read chapter 5 and 6 to familiarize yourself with the concepts of textbook assignments in CHAPTER 5 and 6.

Since there is no system service to print values in hexadecimal representation and we are often looking at Hex values in the MARS simulator, it would seem a Hex Converter progrm might come in handy...

To convert decimal values to Hexadecimal we will need to start with a binary representation of our value and use logical instructions and "bit masking" (ie: Rotate Left, AND) to work our way through the decimal number and convert it to Hex representation...

Recall that a 32-bit binary number can be represented with eight hexadecimal digits. Conceptually, then we need to iterate eight times. Within each iteration, we extract the lower 4 bits from the binary number and then shift the binary number to the right, by 4 bits. We examine the 4 bits that were extracted, and if the value is less than ten, we add the appropriate bias to create the corresponding ASCII code. If the value is ten or greater, then a different bias must be added to obtain the appropriate ASCII code for the correct hexadecimal digit in the range from A through F. Once the ASCII code has been computed, it must be placed into the output buffer, starting at the right most digit position and working to the left.

