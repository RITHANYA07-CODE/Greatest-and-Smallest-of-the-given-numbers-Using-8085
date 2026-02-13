# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:

```
LDA 4200H;
MOV C,A;
LXI H,4201H;
MOV A,M;
INX H;
DCR C;
LOOP:CMP M;
JNC NEXT;
MOV A,M;
NEXT:INX H;
DCR C;
JNZ LOOP;
STA 4300H;
HLT;
```
## Theory:

<img width="905" height="1320" alt="image" src="https://github.com/user-attachments/assets/0ffbecbf-6f6e-4941-8fbd-1e8d110b143d" />

<img width="838" height="1599" alt="image" src="https://github.com/user-attachments/assets/52d865fb-7948-46bb-b320-69bff4d5b2ce" />

<img width="1289" height="745" alt="image" src="https://github.com/user-attachments/assets/1217eba1-aa71-44c1-8e18-b9e4e70ac8ae" />


## Output:

<img width="1731" height="681" alt="image" src="https://github.com/user-attachments/assets/9caa9f96-cfbc-478c-8f44-705c0d2594d0" />

<img width="1728" height="703" alt="image" src="https://github.com/user-attachments/assets/9f6d9d11-2b55-4ab3-b2f6-357b361c08dc" />


## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:

```
LDA 4200H;
MOV C,A;
LXI H,4201H;
MOV A,M;
INX H;
DCR C;
LOOP:CMP M;
JC NEXT;
MOV A,M;
NEXT:INX H;
DCR C;
JNZ LOOP;
STA 4301H;
HLT;
```

## Theory:

<img width="1516" height="1600" alt="image" src="https://github.com/user-attachments/assets/1b0a482b-dc06-4f3d-9127-9d26388e4e84" />

<img width="938" height="1501" alt="image" src="https://github.com/user-attachments/assets/12f37a83-0264-4146-bbb6-827784419a80" />

<img width="1456" height="1600" alt="image" src="https://github.com/user-attachments/assets/32839527-032b-45df-8c44-2d2f5f98fc33" />


## Output:

<img width="1715" height="681" alt="image" src="https://github.com/user-attachments/assets/f2c5ce55-3e82-4f18-a587-a889a4659f75" />

<img width="1741" height="707" alt="image" src="https://github.com/user-attachments/assets/aa89bc2e-3a06-4d01-ae4f-4c64d9ec649c" />


## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
