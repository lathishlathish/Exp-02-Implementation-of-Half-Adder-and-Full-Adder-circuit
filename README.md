## Developed by:  LATHISH KANNA.M
## RegisterNumber:  212222230073
# Exp 03 Implementation of Half Adder and Full Adder circuit


### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Components Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
### Theory:
Adders are digital circuits that carry out addition of numbers.

#### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

#### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure:

1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:*
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6.*Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.

### Program:
#### HalfAdder
```
module HalfAdder(A,B,sum,carry);
input A,B;
output sum,carry;
assign sum= A^B;
assign carry = A&B;
endmodule
```
#### FullAdder
```
module FullAdder(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum= A^B^Cin;
assign carry = (A&B)|((A^B)&Cin);
endmodule
```

### RTL diagram:
#### Half adder
![Screenshot 2023-09-01 083640](https://github.com/Vanitha-SM/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119557985/32bfeadc-25bb-4eaf-ba08-675fe237a1b0)
#### Full adder
![Screenshot 2023-09-01 085358](https://github.com/Vanitha-SM/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119557985/d132e15e-7c20-43a3-bd26-6c14d38e2709)
### Truthtable:
#### Half adder
![WhatsApp Image 2023-09-01 at 08 49 13](https://github.com/Vanitha-SM/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119557985/a856b4b7-5b64-426f-b933-ce0d298e09e5)
#### Full adder
![WhatsApp Image 2023-09-01 at 09 26 40](https://github.com/Vanitha-SM/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119557985/b0f89638-3130-4001-ac5e-4d4c4e8b2a25)

### Output Waveform:
#### Half adder
![Screenshot 2023-09-01 084247](https://github.com/Vanitha-SM/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119557985/ebbc6a8c-59a5-449e-b082-dfe7d05592ec)
#### Full adder
![Screenshot 2023-09-01 085930](https://github.com/Vanitha-SM/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119557985/c8e6c4cb-4cc8-4930-a737-5a7e4131133d)


### Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.


