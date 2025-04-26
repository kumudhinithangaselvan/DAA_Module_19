# EX 1B Merge Sort
## DATE:
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. Start: Read n (number of elements) and input n elements into ar_list.
2. Initialize: Set the initial size to 1, which represents the subarray size for merging.
3. Merge Step: While size is less than the total length:
   Divide the list into pairs of sublists (left and right) of size size.
   Merge each pair using the merge function and update the array.
4. Update Size: Double the size after each full pass through the list.

5. End: After sorting is complete, print the sorted array. 
     

## Program:
```
/*
Program to implement Merge Sort
Developed by: Kumudhini T
Register Number: 212222040084
*/

def merge(left,right):  
    result = []    
    x,y=0,0   
    for k in range(0,len(left)+len(right)):     
        if x==len(left):           
            result.append(right[y])         
            y+=1        
        elif y==len(right):          
            result.append(left[x])        
            x+=1       
        elif right[y]<left[x]:      
            result.append(right[y])         
            y+=1        
        else:           
            result.append(left[x])          
            x+=1   
    return result
def mergesort(ar_list):   
    length=len(ar_list)   
    size=1    
    while size<length:       
        size+=size        
        for pos in range(0,length,size):       
            start=pos           
            mid=pos+int(size/2)          
            end=pos+size           
            left=ar_list[start:mid]           
            right=ar_list[mid:end]           
            print("left: ",left)           
            print("Right: ",right)         
            ar_list[start:end]=merge(left,right)    
    return ar_list
ar_list=[]
n=int(input())
for i in range(n):   
    ar_list.append(int(input()))
print(mergesort(ar_list))
```

## Output:

![2025-04-26 (1)](https://github.com/user-attachments/assets/15c68c7f-0812-4e9b-9d78-b97621c7eaa4)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
