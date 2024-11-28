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

FULL ADDER

![WhatsApp Image 2024-11-28 at 10 56 13_b2206302](https://github.com/user-attachments/assets/e1492482-8423-4cda-838a-845458a45406)

FULL SUBTRACTOR

![WhatsApp Image 2024-11-28 at 10 55 49_0ac6c9e8](https://github.com/user-attachments/assets/c6110642-81ac-4d11-bbbf-a98cbb47bb0d)



**Program:**
**DEVELOPED BY: BALAJI KAMARAJ**
**REG NO : 24901218**


i)FULL ADDER
```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```

ii)FULL SUBTRACTOR
```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & (a ^ b )));
endmodule
```
**RTL Schematic**

FULL ADDER

![WhatsApp Image 2024-11-28 at 10 47 02_2e4c0882](https://github.com/user-attachments/assets/4bfa7478-6d86-4acb-92ed-d6cc95e0a03b)


FUL SUBTRACTER

![WhatsApp Image 2024-11-28 at 10 46 44_afa8db15](https://github.com/user-attachments/assets/9d6729dd-9945-460e-a975-f6c0e45ff5ce)


**Output Timing Waveform**

FULL ADDER

![WhatsApp Image 2024-11-28 at 10 47 02_e9c8d593](https://github.com/user-attachments/assets/dd07c4ca-65ab-49bb-bce4-5d1776bfd395)


FULL SUBTRACTER

![WhatsApp Image 2024-11-28 at 10 45 36_7086c6be](https://github.com/user-attachments/assets/1195dc97-941c-47b0-84a2-3aab53c91873)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
