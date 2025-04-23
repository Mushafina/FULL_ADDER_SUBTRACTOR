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
![WhatsApp Image 2025-04-23 at 20 42 56_6c419b5a](https://github.com/user-attachments/assets/9661e07c-33b7-4e0a-8f22-8c52c97e22da)
![WhatsApp Image 2025-04-23 at 20 43 08_2d18310e](https://github.com/user-attachments/assets/7a8d8355-2464-4eab-9a0e-0b2ee67563cf)

**Procedure**
```
1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram Program:
```
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
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
```
Developed by: Mushafina R 
RegisterNumber:212224220067
*/

**RTL Schematic**

**Output Timing Waveform**
![WhatsApp Image 2025-04-23 at 20 43 31_35b96537](https://github.com/user-attachments/assets/3faf44a1-6822-4dda-bb3e-8aa2d7306bdc)
![WhatsApp Image 2025-04-23 at 20 43 41_29310d5f](https://github.com/user-attachments/assets/b50f73a0-8ad4-4a01-9ec2-74a8ea75c69d)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



