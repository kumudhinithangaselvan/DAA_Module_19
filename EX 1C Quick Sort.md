# EX 1C Quick Sort
## DATE:
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm
1. Start: Read n elements from the user and store them in the array arr.
2. Recursive Sorting: Call the quickSort() function with the full array range (start = 0, end = n).
3. Partitioning: In the partition() function:
   Choose the first element as the pivot.
   Rearrange elements so that smaller values go to the left and larger ones to the right of the pivot.
4. Recursion: Recursively apply quickSort() on the left and right sub-arrays divided by the pivot.
5. Output: After sorting is complete, print the sorted array.
   

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by:Kumudhini T 
Register Number: 212222040084 
*/

def quickSort(alist, start, end):  
    if end - start > 1:      
        p = partition(alist, start, end)       
        quickSort(alist, start, p)       
        quickSort(alist, p + 1, end) 
def partition(alist, start, end):   
    pivot = alist[start]   
    i = start + 1   
    j = end - 1    
    #print("Pivot: ",pivot)   
    while True:       
        while (i <= j and alist[i] <= pivot):            
            i = i + 1       
        while (i <= j and alist[j] >= pivot):       
            j = j - 1        
        if i <= j:           
            alist[i], alist[j] = alist[j], alist[i]       
        else:            
            alist[start], alist[j] = alist[j], alist[start]          
            return j
arr = []
n=int(input())
for i in range(n):   
    arr.append(str(input()))
quickSort(arr, 0, n)
print("Sorted array is:")
for i in arr:  
    print(i)
```

## Output:

![2025-04-26 (3)](https://github.com/user-attachments/assets/66c2da7e-0bc8-4717-8931-50d6daeed986)



## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
