# 19CS301-Module7
EX: 7.1 RECURSION

### Aim:
Write a Python program to convert decimal number to binary number using recursion.

### Algorithm:

Step 1: Start the program.

Step 2: Define a recursive function `decimal_to_binary(n)` to convert a decimal number to binary.

Step 3: Inside the function, check if n is equal to 0.
         - If yes, return an empty string "" (base case).
         
 Step 4: If n is not 0, call the same function recursively with n // 2,
         and concatenate the result with str(n % 2) to build the binary string.
         
 Step 5: Read an integer input from the user and store it in variable n.
 
 Step 6: Call the function `decimal_to_binary(n)` and store the result in `res`.
 
 Step 7: Print the result.
 
 Step 8: End the program.



### Program:
```python
# Name: Nidhish B
# Reg no.: 212223050032
def decimal_to_binary(n):
    if n == 0:
        return "" 
    else:
        return decimal_to_binary(n // 2) + str(n % 2) 
        
n = int(input())
res=decimal_to_binary(n)
print(res)
```
### Output:

![image](https://github.com/user-attachments/assets/9f3ec539-73cd-446c-a70b-a0e111917b41)


### Result:
Thus, the given program is implemented and executed successfully.
 

EX: 7.2 TYPES OF RECURSIONS
### Aim:
To Write a Python program to print odd numbers till ‘N’ using head recursion.

### Algorithm:

 Step 1: Start the program.
 
Step 2: Define a recursive function `fun(n)`.

 Step 3: Inside the function, check if n > 0.
          - If yes, call the function again with n - 2.

 Step 4: After the recursive call, print (n - 1) followed by a space.

 Step 5: Read an integer input from the user and store it in variable x.

 Step 6: If x is even, call `fun(x)`.
         - If x is odd, call `fun(x + 1)` to make it even.

 Step 7: End the program.


STEP 5: Stop.
### Program:
```python

#Name: Nidhish B
#Reg.no: 212223050032

def fun(n):
     if (n >0):
          fun(n - 2)
      print(n-1, end=" ")
x = int(input())
if(x%2==0):
     fun(x)
else:
     fun(x+1)

```
### Output:

![image](https://github.com/user-attachments/assets/27a0b068-633e-4d8b-8b92-bdb6c33275d2)

### Result:

Thus, the given program is implemented and executed successfully.
 


EX: 7.3 TAYLOR SERIES

### Aim:

Write a python program to evaluate the series using recursion: 
1+x+x^2+x^3+.....+x^n by collecting the x and n values from the user.


### ALGORITHM:

 Step 1: Start the program.

Step 2: Define a recursive function `series(x, n)` to calculate the series x^n/n + x^(n-1)/(n-1) + ... + x^1/1 + 1.

Step 3: Inside the function, check if n is equal to 0.
           - If yes, return 1 (base case).

 Step 4: Otherwise, return (x raised to the power n divided by n) plus the recursive call `series(x, n - 1)`.

 Step 5: Read integer inputs for `x` and `n` from the user.

 Step 6: Call the function `series(x, n)` and print the result.

 Step 7: End the program.

### Program:
```python

# Name: Nidhish B
# Reg.no: 212223050032

def series(x,n):
         if n==0:
            return 1
         else:
            return x**n/n+series(x,n-1)
x = int(input())
n = int(input())
print(series(x,n))
```

### Output:
![image](https://github.com/user-attachments/assets/4e2b7c7f-74ab-442c-9aaf-a324c755a37d)

### Result: 
Thus, the given program is implemented and executed successfully .

 

EX: 7.4 Solve by recursion relation

### Aim: 
To Write a Python program to find the product of all elements in the list.

### Algorithm:

1. Start the program.
2. Define a function `prod_list(l, len)` to multiply list elements recursively.
3. If length is 0, return the first element.
4. Else, return l[len] * prod_list(l, len - 1).
5. Create an empty list `l`.
6. Read number of elements `n` from the user.
7. Use a loop to input `n` numbers into the list.
8. Call the function and print the result.
9. End.


### Program:
```python

# Name: Nidhish B
# Reg.no: 212223050032

def prod_list(l,len):
    if len==0:
        return l[0]
    else:
        return l[len]*prod_list(l,len-1)

l=[]
n=int(input())
for i in range(n):
    x=int(input())
    l.append(x)
```
### Output:

![image](https://github.com/user-attachments/assets/5ef9e4d7-190c-4001-aaca-7e5bf3d0a3a2)

### Result:
Thus,the given program is implemented and executed successfully.

EX: 7.4 Solve by tail recursion

### Aim: 
To Write a Python Program to convert a decimal number to a binary number using tail recursion.

### Algorithm:

1. Start
2. Input the decimal number n
3. Define a function con(n) as follows:
    a. If n == 0, return 0
    b. Else, return (n % 2) + 10 * con(n // 2)
4. Call the function con(n) and store the result in res
5. Print the value of res
6. End

### Program:
```python

# Name: Nidhish B
# Reg.no: 212223050032

def con(n):
    if n==0:
        return 0
    else:
        return (n%2)+10*con(int(n/2))

n=int(input())
res=con(n)
print(res)

```
### Output:

![image](https://github.com/user-attachments/assets/ce6f55e8-a797-44cb-a2fa-5146536c86cb)


### Result:
Thus,the given program is implemented and executed successfully.
 

