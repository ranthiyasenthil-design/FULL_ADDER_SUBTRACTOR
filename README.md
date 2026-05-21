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
module exp_3a(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum=A^B^C;
assign carry=((A&B)|(A&C)|(B&C));
endmodule

FULL SUBTRACTOR:
module exp_3b(A,B,C,dif,bor);
input A,B,C;
output dif,bor;
assign dif=A^B^C;
assign bor=(~A&C)|(~A&B)|(B&C);
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: RANTHIYA S RegisterNumber:212225230225
*/
```
module boolean(A,B,C,D,W,X,Y,Z,F1,F2);
 input A,B,C,D,W,X,Y,Z;
 wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
 output F1,F2;
 assign x1=(~A)&(~B)&(~C)&(~D);
 assign x2=(A)&(~C)&(~D);
 assign x3=(~B)&(C)&(~D);
 assign x4=(~A)&(B)&(C)&(D);
 assign x5=(B)&(~C)&(D);
 assign x6=(X)&(~Y)&(Z);
 assign x7=(~X)&(~Y)&(Z);
 assign x8=(~W)&(X)&(Y);
 assign x9=(W)&(~X)&(Y);
 assign x10=(W)&(X)&(Y);
 assign F1=x1|x2|x3|x4|x5;
 assign F2=x6|x7|x8|x9|x10;
 endmodule
```
**RTL Schematic**
FULL ADDER
<img width="1460" height="816" alt="WhatsApp Image 2026-05-21 at 9 08 27 PM" src="https://github.com/user-attachments/assets/a2b3bb99-1f61-4a0f-aec6-51bbed6e205b" />
FULL SUBTRACTOR:
<img width="1461" height="818" alt="WhatsApp Image 2026-05-21 at 9 09 20 PM" src="https://github.com/user-attachments/assets/df4114df-83e9-4faa-aa87-0acc9f61835d" />

**Output Timing Waveform**
FULL ADDER:
<img width="1463" height="825" alt="WhatsApp Image 2026-05-21 at 9 09 46 PM" src="https://github.com/user-attachments/assets/0e2eeed9-f1e1-46ff-83c1-c2a5069e2320" />
FULL SUBTRACTOR:
<img width="1460" height="816" alt="WhatsApp Image 2026-05-21 at 9 10 03 PM" src="https://github.com/user-attachments/assets/ae49506b-8fb7-4711-95dd-f1d1f138b775" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



