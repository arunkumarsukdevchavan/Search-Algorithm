# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```python
''' 
Program for linear search method to match the item in a list
Developed by: ARUN KUMAR SUKDEV CHAVAN
RegisterNumber: 22008531
'''
def linearSearch(array,n,k):
    # write your code for linear search
    for i in range(0,n):
        if (array[i]==k):
            return i
    return -1
array = eval(input())
# sort the array
k = eval(input())# k-item to be seared for
n=len(array)
# get the length of array and store in the variable n
array.sort()
result = linearSearch(array,n,k)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if (result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: ARUN KUMAR SUKDEV CHAVAN
RegisterNumber: 22008531
'''
def binarySearchIter(array, k, low, high):
    # write your code for linear search
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid+1
    return -1
array = eval(input())
# sort the array
array.sort()
print(array)
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
n=len(array)
low=0
high=len(array)-1
result = binarySearchIter(array, k, low, high)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result>=0:
    print("Element found at index: ", result)
else:
    print("Element not found")




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: ARUN KUMAR SUKDEV CHAVAN
RegisterNumber: 22008531
'''
def BinarySearch(arr, k, low, high):
    # Write your code here for binary search using recursive method
    if(high>=low):
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            return BinarySearch(arr, k, mid+1, high)
        else:
            return BinarySearch(arr, k, low, mid+1)
    return -1
    
arr = eval(input())
arr.sort()
print(arr)
#sort the array
k = eval(input()) # k is the element to be searched for
low=0
# use the binary search function to find the result
high=len(arr)-1
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
result=BinarySearch(arr, k, low, high)
if result>=0:
    print("Element found at index: ", result)
else:
    print("Element not found")




```
## Sample Input and Output :
![output](/se1.png)
![output](/se2.png)
![output](/se3.png)





## Result :
Thus the linear search and binary search algorithm is implemented using python programming.