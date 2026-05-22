# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/d21dc941-8e20-4475-b3b4-2aa5a4149ab1" />

<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/9f6396fa-a7c3-4652-a9fc-f3a9715198fd" />

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

6.Write the detailed procedure here

**Program:**

/* 
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:Naveen Kumar V 
RegisterNumber:212225040277


module exp4(a,b,cin,sum,carry,diff,borrow);
input a,b,cin;
output sum,carry,diff,borrow;
wire adash;
not (adash,a);
assign sum = a^b^cin;
assign carry = (a&b)|(b&cin)|(a&cin);
assign diff = a^b^cin;
assign borrow = (adash&b)|(b&cin)|(adash&cin);
endmodule
*/

**RTL Schematic**
<img width="575" height="570" alt="Screenshot 2026-05-22 084644" src="https://github.com/user-attachments/assets/c783a7dc-8f9b-4021-9b4b-1e9daad1b7b8" />


**Output Timing Waveform**

<img width="1909" height="434" alt="image" src="https://github.com/user-attachments/assets/9ce679fe-6d02-4360-9cbc-9a5190e4e3f2" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



