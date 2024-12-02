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

![WhatsApp Image 2024-12-02 at 18 13 29_39b344d8](https://github.com/user-attachments/assets/ce806081-009d-475e-8838-976214d61d4d)



**Procedure**
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: SHARMILA.P             RegisterNumber:24900072
*/
```
module fa(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum=(A^B^Cin);
assign carry=(A&B)|((A^B)&Cin);
endmodule
```
```
module fs(A,B,Bin,diff,borr);
input A,B,Bin;
output diff,borr;
assign diff=(A^B^Bin);
assign borr=((A&B)|((A^B)&Bin));
endmodule
```

**RTL Schematic**

 ![WhatsApp Image 2024-12-02 at 17 51 29_9108e0ed](https://github.com/user-attachments/assets/ea89ebb9-fe37-498c-a391-9ab06a10b4a3)
 ![WhatsApp Image 2024-12-02 at 17 52 26_4f3b85c4](https://github.com/user-attachments/assets/f79bc042-3d02-4c13-8722-e06817b10615)

**Output Timing Waveform**

![WhatsApp Image 2024-12-02 at 17 51 52_c8395d7f](https://github.com/user-attachments/assets/26d21099-8e8e-4564-b31e-a74290f698a5)
![WhatsApp Image 2024-12-02 at 17 52 45_b61c9af4](https://github.com/user-attachments/assets/d4f56fc9-2e21-4313-8f06-e16d9f8984da)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



