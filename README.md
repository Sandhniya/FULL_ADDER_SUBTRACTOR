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

**Procedure**

Write the detailed procedure here

**Program:**
```
/* Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: B.SANDHIYA SREE
RegisterNumber: 212223220093
*/

module FullAddSub(a,b,c,sum,carry,D,BO);
input a,b,c;
output sum,carry,D,BO;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(a&c);
assign D=a^b^c;
assign BO=(~a&b)|(b&c)|(~a&c);
endmodule
```
**RTL Schematic**
![Screenshot 2024-05-06 204159](https://github.com/Sandhniya/FULL_ADDER_SUBTRACTOR/assets/151395890/8177f633-8450-464f-bf6f-843cb8959319)


**Output Timing Waveform**
![Screenshot 2024-05-06 204214](https://github.com/Sandhniya/FULL_ADDER_SUBTRACTOR/assets/151395890/77359ad7-b187-4ea8-be11-9cdb7932112e)


**Result:**
![Screenshot 2024-05-06 204227](https://github.com/Sandhniya/FULL_ADDER_SUBTRACTOR/assets/151395890/40d3f7cd-4ca8-4783-8461-12e1359f91f8)

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



