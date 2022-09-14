# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
## Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Goparapu Lutheesh
RegisterNumber: 212221230029
```
## HALF ADDER
```
module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
```
## FULL ADDER
```
module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```

Logic symbol & Truthtable
RTL realization

## OUTPUT:
### HALFADDEER
### RTL
![164735289-3db068ad-4c62-4d8c-a36e-679dd0df467a](https://user-images.githubusercontent.com/94154531/190225091-7f5774cd-2f9c-458d-91fb-209fb59c0cf9.png)

### TIMING DIAGRAM


### TRUTH TABLE
![164735520-810f282a-4709-451b-82de-52f2bf67ddce](https://user-images.githubusercontent.com/94154531/190225313-b16faf08-1644-4152-a188-68aa19354682.png)

## FULLADDER
## RTL Realization
#![164736025-b0d309d4-55f1-4413-84f2-7d3329db5b04](https://user-images.githubusercontent.com/94154531/190225530-5844a4e3-9e11-4e7d-ba4c-bd13d9f887a4.png)
### Truthtable
![164736152-8ab77950-c466-4859-b58a-89a403b93a23](https://user-images.githubusercontent.com/94154531/190225668-b9d35654-aedf-445e-bf8b-7abd4bde4794.png)
### Timing Diagram

 

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
