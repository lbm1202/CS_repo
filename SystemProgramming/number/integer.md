# integer
Expression of Integer
[end](#end)
1. Usually stored in 1 byte, 2 bytes, 4 bytes, 8 bytes
2. It is divided into signed integer and unsigned integer. 
3. If there is a sign, the first bit indicates the sign (0: positive number, 1: negative number)
***
integer data type range in C
|DataType|size|Range| 
|------|----|-----|
|unsigned char|1byte|0~255| 
|char|1byte|-128~127|
|short|2byte|-32,768~32,767|
|unsigned short|2byte|0~65,535|
|int|4byte|-2,147,483,648~2,147,483,647|
|unsigned int|4byte|0~4,294,967,296|
***
How to make negative integer
- use 2's complement
>Decimal 43 to negative binary

```
    43 == 0b 0010 1011
       -> 0b 1101 0100 (1's complement)
       -> 0b 1101 0101 (2's complement == 1's complement + 1)
    0b 1101 0101 == -43(Decimal)
```

therfore
> 43 + x = 0 ->  x = -43

```
   add
    0b 0010 1011 (43)
    0b 1101 0101 (-43)
    --------------
    0b (1) 0000 0000
   if carry ignore, its fully success 
```

***
binary multiplication
- if nbit multiplication, need 2n bit
> 0b1010 * 0b0101
   (operand1) * (operand2)
```
   0000 | 0101 <- if right most bit is 1, left section + opeerand1 and right shift
   1010+|
   1010 |
   -----|----- shift >> 1
   0101 | 0010 <- if right most bit is 0, right shift
   -----|----- shift >> 1
   0010 | 1001 <- if right most bit is 1, left section + opeerand1 and right shift
   1010+|
   1100 | 1001
   -----|----- shift >> 1
   0110 | 0100 <- if right most bit is 0, right shift
   -----|----- shift >> 1
   0011 | 0010 if shift n amount, then finish
```

***
binary divide & modulo
- if nbit divide & modulo, need 2n bit
- left section is modulo, right section is divide
> 0b0011 / 0b1011
   (operand1) / (operand2)
```
   ? bit == (left section - operand1) >= 0 ? 1 : 0
   left section == (left section - operand1) >= 0 ? (left section - operand1) : left section
   
   0000 | 1011
   -----|----- shift << 1
   0001 | 011? <- 0001 + 1101 = 1110 < 0
   0001 | 0110
   -----|----- shift << 1
   0010 | 110? <- 0010 + 1101 = 1111 < 0
   0010 | 1100
   -----|----- shift << 1
   0101 | 100? <- 0101 + 1101 = 0010 > 0
   0010 | 1001
   -----|-----
   0101 | 001? <- 0101 + 1101 = 0010 > 0
   0010 | 0011
   modulo | divide

   0011 / 1011 == 0011
   0011 % 1011 == 0010
```
#end
