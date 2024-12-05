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
![Screenshot 2024-12-04 222742](https://github.com/user-attachments/assets/c27e2ed7-9f87-4d3a-8552-68846e280f1c)
![Screenshot 2024-12-04 222951](https://github.com/user-attachments/assets/646444b7-26f3-450c-980e-fad8c325aa47)

**Procedure**

Write the detailed procedure here

**Program:**

full adder:
```
module ex4(sum,count,a,b,cin);
output sum;
output count;
input a;
input b;
input cin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign count=w2|w3;
endmodule

```
full subractor:
```
module digital4(a,b,bin,diff,bout);
input a, b, bin;
output diff, bout;
assign diff = a ^ b ^ bin;
assign bout = (~a & b) | (~a & bin) | (b & bin);
endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:TAMILSELVI. I
RegisterNumber:24900261
*/


**RTL Schematic**




![Screenshot 2024-12-04 211723](https://github.com/user-attachments/assets/84c320b2-2591-4ddc-afe5-78a749035a7d).




![Screenshot 2024-12-04 221118](https://github.com/user-attachments/assets/976d6f25-1a72-4b9e-ac9b-c0155404b714)




**Output Timing Waveform**
![image](https://github.com/user-attachments/assets/e6581ddd-68f5-4844-a6c8-e393b70f797f)



![image](https://github.com/user-attachments/assets/32b79a61-b108-44d3-aa6a-9c47d40bc31f)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



