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
Developed by:harish
RegisterNumber: 23013571
'''
def linearsearch(array,n,k):
    # write your code for linear search
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
array = eval(input())
# sort the array
k = eval(input()) # k-item to be seared for
n=len(array)
array.sort()
# get the length of array and store in the variable n
result =linearsearch(array,n,k) # use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:
RegisterNumber: 
'''
def binarySearchIter(array, k, low, high):
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
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
# sort the array
k = eval(input()) #k-item to be searched
result=binarySearchIter(array,k,0,len(array)-1)
# use the binary search function to find the item in the list
if(result==-1):
   print(array)
   print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
    
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: harish
RegisterNumber: 23013571
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch(arr,k,mid+1,high)
    else:
        return -1
    # Write your code here for binary search using recursive method
arr = eval(input())   
#sort the array    
arr.sort()
k = eval(input()) # k is the element to be searched for
result=BinarySearch(arr,k,0,len(arr)-1)
# use the binary search function to find the result
if(result==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result

```
## sample input and output:
![Screenshot 2024-01-02 211522](https://github.com/Harishragaventhira/Search-Algorithm/assets/145548269/e59bbfea-f257-4c42-8bb5-1fb327f0a85f)
![Screenshot 2024-01-02 211537](https://github.com/Harishragaventhira/Search-Algorithm/assets/145548269/75f09ce2-ce74-4ab7-964c-adc671e7b06f)
![Screenshot 2024-01-02 211555](https://github.com/Harishragaventhira/Search-Algorithm/assets/145548269/11b11c7f-133f-40f9-9108-1d464dcfee31)
## output:
![Screenshot 2024-01-02 211638](https://github.com/Harishragaventhira/Search-Algorithm/assets/145548269/78f9ed0b-5b89-44fc-aa41-3187b540b03b)
![Screenshot 2024-01-02 211657](https://github.com/Harishragaventhira/Search-Algorithm/assets/145548269/8695db2d-ea8a-4477-bca9-ad595db00c39)
![Screenshot 2024-01-02 211710](https://github.com/Harishragaventhira/Search-Algorithm/assets/145548269/da830113-ad2a-478e-8cf2-9560970d1499)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
