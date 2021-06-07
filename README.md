# Modbus-2-seperate-registers-to-float32-javascript
This javascript code takes in two seperate registers read from a PLC and combine them to produce the float32 value accordin to the IEE 754 standard.
This does the trick of intepreting float values as it is but consideration should be given to the byte order of the sender. This could be either litle endian or big endian.
