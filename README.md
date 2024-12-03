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

Full Adder

![Screenshot 2024-12-04 003448](https://github.com/user-attachments/assets/4d5b5609-d628-4b60-bfca-02ceaefb4a83)

Full Subtractor

![Screenshot 2024-12-04 003455](https://github.com/user-attachments/assets/d2717084-361c-4c4f-a936-3455f950e2bb)


**Procedure**

Write the detailed procedure here

**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Harish R
RegisterNumber: 24001191
*/
```
Full Adder

```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```
Full Subtractor

```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```
**RTL Schematic**

Full Adder

![Screenshot 2024-12-04 002514](https://github.com/user-attachments/assets/8c21e2b0-9c8e-4d1c-b46a-966a5357a71f)

Full Subtractor

![Screenshot 2024-12-04 003058](https://github.com/user-attachments/assets/c82b7dc0-61dd-4116-ac17-a45052c328d1)


**Output Timing Waveform**

Full Adder

![Screenshot 2024-12-04 002718](https://github.com/user-attachments/assets/16fd86b9-b874-4ea0-ad16-f48f05fb2102)

Full Subtractor

![Screenshot 2024-12-04 003226](https://github.com/user-attachments/assets/e3c5779a-0d2f-4879-bb4c-bd8a79da4a26)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



