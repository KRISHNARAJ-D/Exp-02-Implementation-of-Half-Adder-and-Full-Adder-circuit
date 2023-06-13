# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

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
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: KRISHNARAJ D
RegisterNumber: 212222230070
```
### HALF ADDER
```
module halfadd(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
### FULL ADDER
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
### Output:
## RTL

### HALF ADDER
![1DE](https://user-images.githubusercontent.com/119559695/233263963-ef7ba031-e645-4193-b4ff-d180e0c377b8.png)
### FULL ADDER
![2DE](https://user-images.githubusercontent.com/119559695/233264019-75a8fe45-b6b0-4212-9321-dc069ca8eec6.png)

## TIMING DIAGRAM

### HALF ADDER
![3DE](https://user-images.githubusercontent.com/119559695/233264082-b6b2c209-c0df-4748-b1f0-ea8f8bffb43b.png)

### FULL ADDER
![4DE](https://user-images.githubusercontent.com/119559695/233265071-e3ae2ff4-dab5-4609-802e-1fa54291349b.png)

## TRUTH TABLE 

### HALF ADDER
![5DE](https://user-images.githubusercontent.com/119559695/233264240-bf5cf850-1425-4b13-89a8-379859ad23ef.png)
### FULL ADDER
![6DE-min (1)](https://user-images.githubusercontent.com/119559695/233266016-a4b9a406-973d-450c-88ca-0c55ddf6478a.jpg)

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
