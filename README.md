## Developed by:Nithya shree B
## RegisterNumber:212223220071


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
Truth table for full adder:
![Screenshot 2024-04-05 112006](https://github.com/Balunithu/FULL_ADDER_SUBTRACTOR/assets/161273477/dd54108f-1714-4867-89a5-0df0355a6481)


Truth table for full subtractor:
![Screenshot 2024-04-05 112006](https://github.com/Balunithu/FULL_ADDER_SUBTRACTOR/assets/161273477/9fedb12f-38a8-444f-8815-3a927d7a53e2)

**Procedure**

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder and full subtractor circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

Write the detailed procedure here

**Program:**
```


module FullAddSub(a,b,c,sum,carry,D,BO);
input a,b,c;
output sum,carry,D,BO;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(a&c);
assign D=a^b^c;
assign BO=(~a&b)|(b&c)|(~a&c);
endmodule
```
![Screenshot 2024-04-05 111804](https://github.com/Balunithu/FULL_ADDER_SUBTRACTOR/assets/161273477/019ca5dd-0704-4f63-8cfd-2feaa1642735)

**RTL Schematic**
![Screenshot 2024-04-05 111815](https://github.com/Balunithu/FULL_ADDER_SUBTRACTOR/assets/161273477/7cc1e33a-8744-4660-bb78-4ed4fddd297b)

**Output Timing Waveform**
![Screenshot 2024-04-05 111825](https://github.com/Balunithu/FULL_ADDER_SUBTRACTOR/assets/161273477/2df32623-2f9d-4301-9445-17d6b1b02c86)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



