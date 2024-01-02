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
''' 
Program for linear search method to match the item in a list
Developed by: Yadhav.G.P
RegisterNumber: 23004895
'''
def linearSearch(array,n,k):
    for i in range(n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
array.sort()
k = eval(input())
n=len(array)
print(array)
result = linearSearch(array,n,k)
if result == -1:
    print("Element not found")
else:
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:Yadhav.G.P
RegisterNumber: 23004895
'''
def binarySearchIter(array, k, low,high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
array.sort()
k = eval(input())
print(array)
result=binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Yadhav.G.P
RegisterNumber: 212223230247
'''
def BinarySearch(arr,low, high,x):
    if high>=low:
        mid=(high + low)//2
        if arr[mid]==x:
            return mid
        elif arr[mid]>x:
            return BinarySearch(arr,low,mid-1,x)
        else:
            return BinarySearch(arr,mid+1,high,x)
    else:
        return -1
arr = eval(input())
arr=sorted(arr)
x=eval(input())
result=BinarySearch(arr,0,len(arr)-1,x)
if result!=-1:
    print(arr)
    print("Element found at index: ",str(result))
else:
    print(arr)
    print("Element not found")

```
## Output
1.![Screenshot from 2024-01-02 12-40-39](https://github.com/iamyadhav/Search-Algorithm/assets/147139713/1462c4c2-39ec-4b15-914a-551dd2ec103a)
2.![Screenshot from 2024-01-02 12-41-56](https://github.com/iamyadhav/Search-Algorithm/assets/147139713/8b658690-4720-42ee-acf6-e5f6425bacd0)
3.![Screenshot from 2024-01-02 12-43-09](https://github.com/iamyadhav/Search-Algorithm/assets/147139713/a2bb2034-7b05-4cc4-acb9-a5afd1c0af71)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
