# Reversing-a-Number-using-Recursion-in-Python

Reversing a Number using Recursion
On this page will learn to create Python Program for Reversing a Number using Recursion as well as loop.

Note : That the given program doesn’t consider leading zeroes. For example, for 100 program will print 1. If you want to print 001 then remove the int from print statement.

Example :

Input : 12345
Output : 54321
Explanation : Reverse of 12345 is 54321
Reverse Number in Python

Method 1 : Using Recursion
Algorithm
Start by converting number to list named as arr and passing the list, half of length of arr to a function
As value of n is not passed to function so it is set by default to 0
If n is equals to l return arr
Swipe the values of arr[n] and arr[-1*(n+1)]
Return the value of recursive call for same function with values passed arr, l, n+1
Convert the returned list to integer and Print
Python Program to Reversing a Number
To Learn more about Recursion   click here
Python Code
Run
def reverse_digit(arr, l, n=0):
    if n == l:
        return arr
    arr[n], arr[-1*(n+1)] = arr[-1*(n+1)], arr[n]
    return reverse_digit(arr, l, n + 1)


num = 12345
arr = list(str(num))
arr = reverse_digit(arr, len(arr)//2)
s = ""
print(int(s.join(arr)))
Output :

Reverse of 12345 is 54321
Method 2 : Using Loop
Algorithm
Start by converting number to list named as arr and passing the list, half of length of arr to a function
Iterate from range 0 to l using variable i
Swipe the value of arr[i] and arr[-1*(i+1)]
Return arr
Convert the returned list to integer and Print
Python Code
Run
def reverse_digit(arr, l):
    for i in range(l):
        arr[i], arr[-1 * (i + 1)] = arr[-1 * (i + 1)], arr[i]
    return arr


num = 12345
arr = list(str(num))
arr = reverse_digit(arr, len(arr)//2)
s = ""
print(int(s.join(arr)))
Output :

Reverse of 12345 is 54321
