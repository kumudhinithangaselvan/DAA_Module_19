# EX 1A Reverse a String
## DATE:
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm
1. Start: Read two integers, n (base) and x (exponent).
2. Check: If x is 0, return 1 (since anything raised to 0 is 1).
3. Recursive Call: Otherwise, recursively multiply n with the result of power(n, x-1).
4. Compute: Continue this process until the exponent reaches 0.
5. Output: Print the result using a formatted message.
   

## Program:
```
/*
Program to implement Reverse a String
Developed by: Kumudhini T
Register Number: 212222040084 
*/
def power(num, topwr):
    if topwr==0:
        return 1;
    else:
        return num*power(num,topwr-1)
n=int(input())
x=int(input())

print('{} to the power of {} is {}'.format(n, x, power(n, x)))
```

## Output:

![image](https://github.com/user-attachments/assets/52c36330-8f71-4bdf-b851-067d12c5bd09)


## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
