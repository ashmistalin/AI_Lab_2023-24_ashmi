![image](https://github.com/ashmistalin/AI_Lab_2023-24_ashmi/assets/103128410/052e4501-f018-4f4c-b6aa-ad44aacf7b1c)# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE: 18-03-24                                                                           
### REGISTER NUMBER : 212221040021
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:

## HALF ADDER , HALF SUBTRACTOR:
```
and(0,0,0).
and(0,1,0).
and(1,1,1).
and(1,0,0).
xor(0,0,0).
xor(0,1,1).
xor(1,0,1).
xor(1,1,0).
not(0,1).
not(1,0).
halfadder(A,B,S,C):-
    xor(A,B,S),
    and(A,B,C).
halfsubtractor(A,B,Diff,Bo):-
    xor(A,B,Diff),
    not(A,X),
    and(B,X,Bo).

```
## FULL ADDER:
```
full_adder(A, B, Cin, Sum, Cout) :-
    half_adder(A, B, S1, C1),
    half_adder(S1, Cin, Sum, C2),
    or(C1, C2, Cout).

half_adder(A, B, Sum, Carry) :-
    xor(A, B, Sum),
    and(A, B, Carry).

xor(0, 0, 0).
xor(0, 1, 1).
xor(1, 0, 1).
xor(1, 1, 0).

and(0, 0, 0).
and(0, 1, 0).
and(1, 0, 0).
and(1, 1, 1).

or(0, 0, 0).
or(0, 1, 1).
or(1, 0, 1).
or(1, 1, 1).
```

### Output:

## HALF ADDER:
![Screenshot (536)](https://github.com/DrUmaRaniV/AI_Lab_2023-24/assets/103128410/073e9736-3e27-443f-bf2e-4e6cec3eb3b6)

## HALF SUBTRACTOR:
![Screenshot (537)](https://github.com/DrUmaRaniV/AI_Lab_2023-24/assets/103128410/605073e5-3576-45b3-bfd0-c0c8e2cb918b)

## FULL ADDER:


### Result:
Thus the truth table of circuit verified sucessfully.
