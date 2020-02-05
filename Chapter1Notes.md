[Back to index](/Readme.md)

# Chapter 1

## Decimal
Base 10

How many values: 10n

Range: 0 - 10n-1, [0, 10n-1]

## Binary
Base 2

1 - true, high

0 - false, low

How many values: 2n

Range: 0002 - 2n-1

## Hexadecimal
Base 16

0-9, A-F

Convert 2910 -> hex
11101 -> 0x1D


### Datatypes
Byte: 8 bits - 2 Hex
Nibble: 4 bits - 1 Hex
Word: 2 bytes - 4 Hex
Doubleword: 4 bytes - 8 Hex
Quadword: 8 bytes - 16 Hex

## Binary Addition
```
 11
1011
0011
1110
```
```
  1
1001
0101
1110
```
```
1 1 
 1011
 0110
10001
```

## Signed Numbers
### Sign/Magnitude
- Most significant bit is the sign bit
- Positive number: sign bit = 0
- Negative number: sign bit = 1
- +6 = 0110
- -6 = 1110

### Two’s Compliment

Take the binary representation, flip the bits, then add 1

- 3 = `0011`
- -3 = `1101`

- 6 = `0110`
- -6 = `1010`

- `1001` = -7

```
11    11
0110  1110   
1010  0011
0000  0001
```

### Increasing Bit Width
#### Sign-Extension
Copy sign bit to the new bits
#### Zero-Extension
Fill new bits with zeroes

## Circuits
### Single Input
#### NOT

`Y = ~A`

|A|Y|
|-|-|
|0|1|
|1|0|

#### BUF

`Y = A`

|A|Y|
|-|-|
|0|0|
|1|1|

### Two Input
#### AND

Requires both inputs to be `true` to output `true`

`Y = AB`

|A|B|Y|
|-|-|-|
|0|0|0|
|0|1|0|
|1|0|0|
|1|1|1|
#### OR

If either input is `true`, the output will be `true`

`Y = A + B`
  
|A|B|Y|
|-|-|-|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

#### XOR

If only one input is `true`, the output will be `true`

`Y = A (+) B`

|A|B|Y|
|-|-|-|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|

#### NAND

If both inputs are `true`, the output will be `false`

`Y = ~(AB)`

|A|B|Y|
|-|-|-|
|0|0|1|
|0|1|1|
|1|0|1|
|1|1|0|

#### NOR

If either input is `true`, the output will be `false`

`Y = ~(A + B)`

|A|B|Y|
|-|-|-|
|0|0|1|
|0|1|0|
|1|0|0|
|1|1|0|

#### XNOR

If only one input is `true`, the output will be `false`.
If neither input is `true` or both inputs are `true`, the output will be `true`

`Y = ~(A (+) B)`

|A|B|Y|
|-|-|-|
|0|0|1|
|0|1|0|
|1|0|0|
|1|1|1|

#### NOR3

`Y = ~(A + B + C)`

|A|B|C|Y|
|-|-|-|-|
|0|0|0|1|
|0|0|1|0|
|0|1|0|0|
|0|1|1|0|
|1|0|0|0|
|1|0|1|0|
|1|1|0|0|
|1|1|1|0|