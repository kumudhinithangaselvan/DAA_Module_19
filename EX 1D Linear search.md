# EX 1D Linear search
## DATE:
## AIM:
To write a python program for a search function with parameter list name and the value to be searched using string values.



## Algorithm
1.Start: Read n (number of elements) and input n floating-point numbers into a list.
2. Input Key: Read the key element to search for.
3. Search: Traverse the list from index 0 to n-1, comparing each element with the key.
4. Result:
   If a match is found, return the index.
   If no match is found after checking all elements, return -1.
5. Output: Based on the result, print whether the key was found or not. 
   

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by:Kumudhini T 
Register Number: 212222040084
*/

def LS(list,n,key):
    for i in range(0,n):
        if list[i]==key:
            return i
    return -1
list=[]
n=int(input())
for i in range(0,n):
    ele=float(input())
    list.append(ele)
key=float(input())
res=LS(list,n,key)
if(res==-1):
    print(f"Tuple: {key} not found")
else:
    print(f"Tuple: {key} found")
```

## Output:

![2025-04-26 (4)](https://github.com/user-attachments/assets/57821616-733d-4ad2-ad24-92f6f66614ab)



## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
