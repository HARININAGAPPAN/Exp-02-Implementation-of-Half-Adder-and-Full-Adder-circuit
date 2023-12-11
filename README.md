# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Harini.N
RegisterNumber:  23013709
*/

```
module EX03DEHA(A,B,sum,carry);
input A,B;
output sum,carry;
xor(sum,A,B);
and(carry,A,B);
endmodule

module EX03DEFA(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=((a^b)^c);
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```

### RTL
![Screenshot 2023-12-11 163631](https://github.com/HARININAGAPPAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473910/cc5cc5b6-7c68-4e6c-8861-73fa0b5f4a06)
### TIMING DIAGRAM
![Screenshot 2023-12-11 163811](https://github.com/HARININAGAPPAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473910/dc88b498-7fb6-4eec-b572-8031d7a95a36)

![Screenshot 2023-12-11 163945](https://github.com/HARININAGAPPAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473910/2521cad8-3314-4a05-80fe-7959f6f97a0d)


### TRUTH TABLE:
![Screenshot 2023-12-11 164057](https://github.com/HARININAGAPPAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473910/271584bf-af30-46fd-82f1-169bf91fc467)
### Result:
Thus the implementation of Half Adder and Full Adder verified successfully.


