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
*/
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by:THARIKA S
RegisterNumber:22001698 
HALF ADDER:

module halfadd(a,b,sum,carry);

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule

FULL ADDER:

module fulladder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum = ((a^b)^c);

assign carry = ((a&b)|(b&c)|(c&a));

endmodule
*/
OUTPUT:


Logic symbol & Truthtable:
Half Adder:
![image](https://user-images.githubusercontent.com/119475507/214545272-7be6a8dd-bfd2-4afa-97e3-3af02a00d5fc.png)
Full Adder:
![image](https://user-images.githubusercontent.com/119475507/214545394-904724bc-33c8-49c9-9c96-c8794d97abbe.png)

RTL realization
Half Adder:
![image](https://user-images.githubusercontent.com/119475507/214545545-7cf2daed-2b8a-49cc-a4fc-8edcb39ade67.png)
Full Adder:
![image](https://user-images.githubusercontent.com/119475507/214545634-8af08faf-d341-444f-a5bd-f3563ad1ba09.png)

### TIMING DIAGRAM
Half Adder:
![image](https://user-images.githubusercontent.com/119475507/214545947-e70d1df2-d4be-4a5a-af3b-0a6293303267.png)
Full Adder:
![image](https://user-images.githubusercontent.com/119475507/214546002-2454c4d4-6991-44ea-9789-dc98d1063522.png)


### TRUTH TABLE 
![image](https://user-images.githubusercontent.com/119475507/214546071-9cec85c9-3c1b-4d2b-8447-09579f349fba.png)


### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
