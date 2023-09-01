## Developed by:  LATHISH KANNA.M
## RegisterNumber:  212222230073

# Exp 03 Implementation of Half Adder and Full Adder circuit
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
### 
Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by:  LATHISH KANNA.M
RegisterNumber:  212222230073

HALF ADDER:
module Halfadder(A,B,Sum,Carry);
input A,B;
output Sum,Carry;
xor Sum=A^B;
and Carry=A&B;
endmodule

Full adder:
module fulladder(A,B,C,Sum,Carry);
input A,B,C;
output Sum,Carry;
assign Sum = ((A^B)^C);
assign Carry = ((A&B)|(B&C)|(C&A));
endmodule
```
### TRUTH TABLE
#### HALF ADDER:
![211635229-f50fcf6a-4628-430f-802a-4892a532d3f7](https://github.com/mathes6112004/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119477782/52932227-3c9a-4298-8c06-7409af0349e5)
#### FULL ADDER:
![211637987-62b2ce50-d0e4-4931-9d61-ff2710e43297](https://github.com/mathes6112004/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119477782/eadecf25-ad73-4d1d-8ea7-5d605f511194)

### Output:
#### HALF ADDER:
![Screenshot 2023-09-01 084408](https://github.com/mathes6112004/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119477782/1683402b-1705-4b8b-89f1-42266f967dab)
#### FULL ADDER:
![Screenshot 2023-09-01 090224](https://github.com/mathes6112004/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119477782/5afef56c-b5f8-4f85-a00d-c03575afd02b)

### TIMING DIAGRAM
#### HALF ADDER:
![Screenshot 2023-09-01 084212](https://github.com/mathes6112004/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119477782/8dd845ff-92d2-4b7f-8f42-bcea7d25889d)
#### FULL ADDER:
![2](https://github.com/mathes6112004/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119477782/4c21f81d-ecf7-4395-b811-dba959877a3f)

### Result:
Thus the half adder and full adder circuits are designed and the truth tables is verified using quartus software.

