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
```
Program for linear search method to match the item in a list
Developed by: KEERTHANA S
RegisterNumber: 22009006
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i] == k):
            return i
    return -1

array = eval(input())
k = eval(input())
n = len(array)
array.sort()
result = linearSearch(array,n,k)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: KEERTHANA S
RegisterNumber: 22009006
'''
def binarySearchIter(array, k, low, high):
    while low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
             low = mid + 1
        else:
             high = mid - 1
    return -1
array = eval(input())
array.sort()
k = eval(input())
result = binarySearchIter(array, k, 0, len(array)-1)
if(result == -1):
    print(array)
    print("Element not found")
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Program to find the element in a list using Binary Search (recursive Method).
Developed by: KEERTHANA S
RegisterNumber: 22009006
'''
def BinarySearch(arr, k, low, high):
    # Write your code here for binary search using recursive method
    if high >= low:
        mid = low + (high - low)//2
        if arr[mid] == k:
            return mid
        elif arr[mid] > k:
            return BinarySearch(arr, k, low, mid-1)
        else:
            return BinarySearch(arr, k, mid + 1, high)
    else:
        return -1

arr = eval(input())
arr.sort()
#sort the array
k = eval(input()) # k is the element to be searched for

# use the binary search function to find the result

result = BinarySearch(arr, k, 0, len(arr)-1)
if(result == -1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)

```
## Sample Input and Output

### Input:
i) Linear search method.
![Q1](https://user-images.githubusercontent.com/119477890/214060930-9865fac5-efa2-4150-bf54-99335c5154c1.png)

ii) Binary Search (Iterative Method).
![Q2](https://user-images.githubusercontent.com/119477890/214060963-ac90ca4d-7472-4be1-a3e9-04c461351cac.png)

iii) Binary Search (Recursive Method).
![Q3](https://user-images.githubusercontent.com/119477890/214060998-42bf8946-f3f4-4b2b-ad96-00f7297acb5b.png)


### Output:
i) Linear search method.
![A1](https://user-images.githubusercontent.com/119477890/214061090-b27e51eb-0951-429d-8bb0-6160993036f0.png)

ii) Binary Search (Iterative Method).
![A2](https://user-images.githubusercontent.com/119477890/214061118-964fbc7e-59b2-4575-8cf4-4736c08cd1dd.png)

iii) Binary Search (Recursive Method).
![A3](https://user-images.githubusercontent.com/119477890/214061176-0d0ed6ed-b5f0-4bea-a5ed-a0baa1e23136.png)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
