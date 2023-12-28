![292768502-5e672719-40cf-47ce-8ecb-29b83c5fae1a](https://github.com/Nithish23013509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149038138/175d5293-fe4d-4626-ab40-051b53d33953)# NAME: NITHISH S
# REFERENCE NUMBER:23013509
# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.
# PROCEDURE 
1. TYPE THE PROGRAM IN QUARTUS SOFTWARE.
2. COMPILE AND RUN THE PROGRAM.
3. GENERATE THE RTL SCHEMATIC AND SAVE THE LOGIC DIAGRAM.
4. CREATE NODES FOR  INPUTS AND OUTPUTS TO GENERATE THE TIMING DIAGRAM.
5. FOR DIFFERENT INPUT COMBINATIONS,GENERATE THE TIMING DIAGRAM

## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y
# PROGRAM
```
module project_4_1(a,b,borrow,diff);
input a,b;
output borrow,diff;
assign borrow=~a&b;
assign diff=a^b;
endmodule
```
# RTL REALIZATION
![292768502-5e672719-40cf-47ce-8ecb-29b83c5fae1a](https://github.com/Nithish23013509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149038138/d5d74c9d-95b9-4f8d-9fa0-3e0e6b8deef5)
# TRUTH TABLE

![292768511-b11a9dfc-cc81-4799-9c8f-ad05a0f62db1](https://github.com/Nithish23013509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149038138/ab7bb68b-8291-419e-a666-73a6cf06e67d)
# TIMING DIAGRAM
![292768549-fa31fe80-49a5-4616-9ccf-6d4708897632](https://github.com/Nithish23013509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149038138/537e6b00-3f2b-4e9c-9a19-7123daa7037e)


## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Program:
```
module project_4_2(a,b,bin,borrow,diff);
input a,b,bin;
output diff,borrow;
assign diff=(a^b)^bin;
assign borrow=((~a)&&bin)||(b&&bin)||((~a)&&b);
endmodule
```
## Truthtable
![292768641-0b190dfe-0ae3-4cea-8799-63d14fd42175](https://github.com/Nithish23013509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149038138/0825da0e-ffa6-40ac-8b34-fabc2eed722b)



##  RTL realization
![292768632-4387c7fe-0d95-4f75-89e2-8ec6200d55c8](https://github.com/Nithish23013509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149038138/75c2639c-019f-4914-9380-fa8ce8c4c363)


## Timing diagram 

![292768651-ed397c38-b97d-4655-88c0-77c69dba6521](https://github.com/Nithish23013509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149038138/b1725f34-a779-4438-8d7f-cc453c1cf34b)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
