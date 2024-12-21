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
<img width="659" alt="image" src="https://github.com/user-attachments/assets/9ee36ecf-d70c-43fb-97e4-044314aa3607">


**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.


Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin
<img width="770" alt="image" src="https://github.com/user-attachments/assets/e04b739d-94a6-4ff9-85e9-24907d0c49f3">

**Truthtable**
<img width="727" alt="image" src="https://github.com/user-attachments/assets/545d75ba-f506-4ba2-83da-0c65a40c72a5">
<img width="726" alt="image" src="https://github.com/user-attachments/assets/8fa9d4f5-1241-42b6-b07c-c6371b934985">

**Procedure**

Write the detailed procedure here
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
```
i)full adder
module exp4(
input a,b,c,
output sum,carry);
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=b&c;
assign w3=c&a;
assign carry=w1|w2|w3;
endmodule

ii)full subtractor
module experiment4(a,b,c,diff,borr);
input a,b,c;
output diff,borr;
wire w1,w2,w3,w4,w5,w6;
xor g1(diff,a,b,c);
and g2(w4,w1,b);
and g3(w5,w1,b);
and g4(w6,b,c);
or g5(borr,w4,w5,w6);
endmodule

````
 Developed by:S.NITHYASREE 
 RegisterNumber:24900149
*/
**RTL Schematic**

**Output Timing Waveform**
<img width="960" alt="image" src="https://github.com/user-attachments/assets/fcc3bfc3-2b2f-4c57-a59a-91dd54418f12">
<img width="955" alt="image" src="https://github.com/user-attachments/assets/15c87ec0-3fbc-4c47-9150-1f794ae9c112">



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



