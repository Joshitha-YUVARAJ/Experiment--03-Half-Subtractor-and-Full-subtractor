# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

1)HALF SUBTRACTOR
Simulator 1:
Step-1) Connect the Supply(+5V) to the circuit.
Step-2) First press "ADD" button to add basic state of your output in the given table.
Step-3) Press the switches to select the required inputs "A" and "B".
Step-4) Press "ADD" button to add your inputs and outputs in the given table.
Step-5) Repeat steps 3&4 for next state of inputs and their corresponding outputs.
Step-6) Press the "PRINT" button after completing your simulation to get your results.


Simulator 2:
Step-1) Enter the Boolean input "A" and "B".
Step-2) Enter the Boolean output for your corresponding inputs.
Step-3) Click on "Check" Button to verify your output.
Step-4) Click "Print" if you want to get print out of Truth Table.
Step-5) Click "Reset" if you want to reset inputs and outputs.
2)FULL SUBTRACTOR
Simulator 1:
Step-1) Connect the Supply(+5V) to the circuit.
Step-2) First press "ADD" button to add basic state of your output in the given table.
Step-3) Press the switches to select the required inputs "A" and "B" and "Bin".
Step-4) Press "ADD" button to add your inputs and outputs in the given table.
Step-5) Repeat steps 3&4 for next state of inputs and their corresponding outputs.
Step-6) Press the "PRINT" button after completing your simulation to get your results.


Simulator 2:
Step-1) Enter the Boolean inputs "A" and "B" and "Bin".
Step-2) Enter the Boolean output for your corresponding inputs.
Step-3) Click on "Check" Button to verify your output.
Step-4) Click "Print" if you want to get print out of Truth Table.
Step-5) Click "Reset" if you want to reset inputs and outputs.

 


## Program:

/*

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:YUVARAJ JOSHITHA 

RegisterNumber:  

*/

HALF SUBTRACTOR:

```
module half_sub(output bo,d,input a,b);
assign d= a^b;
assign bo=~a&b;
endmodule
```
FULL SUBTRACTOR:

```
module full_sub(output d,bo,input a,b,c);
assign d = a^b^c;
assign bo = ~a&(b^c)|b&c;
endmodule
```
## Output:

## Truthtable

HALF SUBTRACTOR:

![Screenshot 2023-12-01 194259](https://github.com/Joshitha-YUVARAJ/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145742770/1e71ddfd-8d8b-4c49-9b75-94351e61b398)



FULL SUBTRACTOR:

![Screenshot 2023-12-01 194345](https://github.com/Joshitha-YUVARAJ/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145742770/4af58087-f3a4-4fd6-8082-8737efcb3faf)



##  RTL realization

HALF SUBTRACTOR:

![Screenshot 2023-12-01 145223](https://github.com/Joshitha-YUVARAJ/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145742770/b2bc3ce7-e8a9-4b3d-a349-73192c3394eb)

FULL SUBTRACTOR:

![Screenshot 2023-12-01 193441](https://github.com/Joshitha-YUVARAJ/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145742770/f98891da-84c7-450b-b7c3-e28aad51a301)


## Timing diagram 

HALF SUBTRACTOR:

![Screenshot 2023-12-01 145435](https://github.com/Joshitha-YUVARAJ/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145742770/45598a36-05d8-4245-a833-9239beec75ee)

FULL SUBTRACTOR:

![Screenshot 2023-12-01 193855](https://github.com/Joshitha-YUVARAJ/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145742770/ac4d7b49-6aa1-468d-87fb-d4ca0199536d)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
