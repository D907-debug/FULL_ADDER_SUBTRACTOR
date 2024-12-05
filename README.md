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



**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:K.Dilli Babu:24900561
*/
1.full adder
module FULLADDER(sum, cout, a, b, cin);
input a;
input b;
input cin;
output sum;
output cout;
wire w1,w2,w3;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign cout=w2|w3;
endmodule
2. full subtractor
module FULLSUBTRACTOR(a, b, cin, diff, borrow);
input a;
input b;
input cin;
output diff;
output borrow;
wire abar;
assign abar= ~ a;
assign diff=a^b^cin;
assign borrow=(abar & b) | (b & cin) |(cin & abar);
endmodule
'''

**RTL Schematic**

 1.FULL ADDER
 '''
 ![Screenshot 2024-12-05 164430](https://github.com/user-attachments/assets/f0b873fe-96e5-400b-b9bc-0fe2f19d0a39)
 '''
 2.FULL SUBRACTER
 '''
 ![Screenshot 2024-12-05 164449](https://github.com/user-attachments/assets/560fa923-8170-41e9-8970-4cdfec577c27)

'''
**Output Timing Waveform**
1.FULL ADDER
'''
![Screenshot 2024-12-05 164508](https://github.com/user-attachments/assets/afccf456-0e5c-4dfc-8866-717f21b16f9b)
'''
2.FULL SUBRACTER
'''
![Screenshot 2024-12-05 164532](https://github.com/user-attachments/assets/7924fb63-b618-4c27-ba7b-204ab40c2439)
'''



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



