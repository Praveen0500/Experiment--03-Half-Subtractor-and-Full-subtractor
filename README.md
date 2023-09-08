# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

STEP 1: Use module project name(input,output) to start the Verilog programmming.

STEP 2: Assign inputs and outputs using the word input and output respectively.

STEP 3: Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

STEP 4: Use each output to represnt onre for differnce and the other for borrow.

STEP 5: End the verilog program using keyword endmodule.


## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: PRAVEEN S 

RegisterNumber: 212222240078

### half subractor:
```
module ex4(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule
```
### full subractor:
```
module exp4(a,b,bin,diff,borrow);
input a,b,bin;
output diff,borrow;
assign diff = (a^b^bin);
assign borrow = (~a&b)|(~(a^b)&bin);
endmodule
```
## Output:

## Truthtable

### half subractor

![ha](https://github.com/Praveen0500/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120218611/0ac1ac6a-1e5b-4b80-9246-a1026e0fb65e)

### full subractor
![fu](https://github.com/Praveen0500/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120218611/36f561e9-0ea3-4dd8-8857-8b3e85710775)



##  RTL realization

### half subractor 
![rtl 4](https://github.com/Praveen0500/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120218611/151300a7-3d36-4551-a668-36ad9fe1106b)


### full subractor

![rtl 4 1](https://github.com/Praveen0500/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120218611/1ecfdc2a-be1c-4ddc-a607-278288e749aa)



## Timing diagram 

### half subractor

![wave 4](https://github.com/Praveen0500/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120218611/1cc1cddc-d4d0-40ee-97a9-5c7d6b0fcce0)

### full subractor
![wave 4 1](https://github.com/Praveen0500/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120218611/cf121b9a-33aa-411f-ac4f-8e25ac946dd1)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
