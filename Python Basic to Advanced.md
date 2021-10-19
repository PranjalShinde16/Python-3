### Print HelloWorld


```python
print("Helloworld")
```

    Helloworld
    

### Add two numbers


```python
a = 10
b = 20
print(a+b)
```

    30
    


```python
a = 20
b = 5
a+b 
```




    25



A variable name can start with _ , a , A but cannot start with a digit
a # can comment out a code

### Assigning different type of data to a variable


```python
a = 10
a = 20
a = "changed the data type"
print(a)
```

    changed the data type
    

In C++ compiler allot space for a particular datatype. For ex. 4 byte for int
but in python compiler allot new location everytime a variable is declared and variable stores new address of location


```python
print(type(a))
# a was previously executed as a string
a = 10.3
print(type(a))
```

    <class 'float'>
    <class 'float'>
    

### Python Numbers


```python
a1 = 10 + 2j
print(type(a1))
a2 = 23
a3 = 3.4
print(type(a2))
print(type(a3))
```

    <class 'complex'>
    <class 'int'>
    <class 'float'>
    

complex numbers are also allowed in python


```python
a = 10
print(id(a))
a = a + 1
print(id(a)) #here the storage is changed while adding
print(a) 
```

    140721900496976
    140721900497008
    11
    


```python
#id are same here
a = 10
b = 10
print(id(a))
print(id(b))
```

    140721900496976
    140721900496976
    


```python
a = 10
b = id(a)
print(b)
```

    140721900496976
    

 We can store a very large number in python because of its dynamic allocation property

### Arithmatic Operators


```python
10 == 100
```




    False




```python
a = 20
b = 3
print(a/b) #floating division
print(a//b) #integer division
print(a**b) #to the power (exponentiation)
print(a%b) #modulus
```

    6.666666666666667
    6
    8000
    2
    

Python follows the BODMAS rule


```python
2 + 3 * 4
```




    14




```python
2 * 3 // 4 #when operations are of same weightage then operations take place sequentially
```




    1



## Function on string


```python
str1 = "ab"
str2 = "cd"
print(str1 + str2)
```

    abcd
    

## Input


```python
input()
```

    23
    




    '23'




```python
a = input()
print(type(a)) #type will be string
print(a)
a = int(a)
print(type(a)) #changed type to int
print(a)
```

    23
    <class 'str'>
    23
    <class 'int'>
    23
    


```python
a = input()
b = input()
print(int(a)+int(b))
```

    10
    20
    30
    


```python
a = int(input())
b = int(input())
print(a+b)
```

    10
    20
    30
    

## Booleans


```python
a = True
b = False
print(type(a))
```

    <class 'bool'>
    

## Relational Operators


```python
a = input()
b = input()
print(a>b)
print(b>a)
print(a==b)
print(a>=b)
print(b>=a)
print(a!=b)
```

    10
    10
    False
    False
    True
    True
    True
    False
    

## Logical Operators


```python
a = 10
b = 20
c1 = a > 10
c2 = b > 10
print(c1 and c2)
print(c1 or c2)
print(not c2)
```

    False
    True
    False
    

## If Else Statements


```python
a = False
if a:
    print("A is True") #Indentation is very important in python
else:
    print("A is False")
```

    A is False
    

Using if condition without any else is also OK

## Else if Statements and Nested If Else


```python
a = int(input())
if a>10:
    if a>20:
        print("It is greater than 20")
    else:
        print("Lies between 10 and 20")
elif a>5:
    print("Lies between 5 and 10")
else:
    print("Less than 5")
```

    2
    Less than 5
    

## While Loops


```python
n = 5
while (n>0):
    print(n)
    n = n - 1
```

    5
    4
    3
    2
    1
    

## Print kth alphabet


```python
k = int(input())
# 'A' + k - 1
a = ord('A')
a = a + k - 1
print(chr(a))
```

    2
    B
    

## For loop


```python
x = input()
for i in x:
    print(i) #acting as for(auto& x : vect)
```

    abc
    a
    b
    c
    


```python
n = int(input())
for i in range(0,n+1,1):
    print(i," ",end='') #normal for(ll i=0;i<n+1;i++)
```

    3
    0  1  2  3  

for i in range(start,end,step), by default start is 0,step is 1


```python
n = int(input())
for i in range(n,0,-1):
    print(i," ",end='')
```

    3
    3  2  1  

## Break


```python
n = int(input())
for i in range(0,n+1,1):
    print(i,' ',end='')
    if(i==n/2):
        break
```

    6
    0  1  2  3  

## Else


```python
i = 1
while i<=10:
    print(i," ",end='')
    i = i + 1
else:
    print()
    print("This will be printed at the end (once)")
```

    1  2  3  4  5  6  7  8  9  10  
    This will be printed at the end (once)
    


```python
#Code inside the else will not be executed if the while loop is terminated by break#
i = 1
while(i<10):
    print(i)
    i = i + 1
    if(i==5):
        break;
else:
    print("Print this once")
```

    1
    2
    3
    4
    

## Continue


```python
#Used of skip an iteration
for i in range(0,10,1):
    print(i,end='')
    if(i==2):
        continue
    print(i)
```

    00
    11
    233
    44
    55
    66
    77
    88
    99
    

## Pass


```python
n = 2
if (n<3):
    pass
print("Hey")
```

    Hey
    

## Functions


```python
#finding nCr using function
def fact(n):
    ans = 1
    for i in range(1,n+1,1):
        ans = ans * i
    return ans
n = int(input())
r = int(input())
n_fact = fact(n)
r_fact = fact(r)
n_r_fact = fact(n-r)
ans = n_fact//(r_fact*n_r_fact)
print(ans)
```

    5
    2
    10
    


```python
fact(10) #It is still working since we have defined fact() in last code
```




    3628800




```python
def f2():
    n = int(input())
    print(n)
def f1():
    n = int(input())
    f2()
    print(n)
f1()
```

    10
    20
    20
    10
    

## Local and Global variables


```python
#you can access any global variable defined before the function call
a = 10 #Global Variable
def f1():
    b = 12 #Local Variable
```


```python
a = 13
def f():
    a = 12  #Python assumes that you want to create a local variable
    print(a) #You can try printing the id for confirmation
print(a)
f()
print(a)
```

    13
    12
    13
    


```python
a = 13
def f():
    global a
    a = 12  #Now the change is made in global variable
    print(a)
print(a)
f()
print(a)
```

    13
    12
    12
    

## Default Argument


```python
def sum(a,b,c=0):  #Here c is defined with default value
    return a + b + c
print(sum(1,2,3))
print(sum(1,2))
```

    6
    3
    

By rule the non-default arguements should be before arguments with default value
For ex :
f(a = 0,b,c) is not correct


```python
def f(a,b,c=2,d=0):
    return a + b + c + d
print(f(1,2,3,4))
print(f(1,2))
print(f(2,3,d=7))
```

    10
    5
    14
    

## Lists


```python
#Python Lists need not homogeneous data, heterogeneous data can be stored
#1,2.4,"John",4
list = []
lis = [1,2,3]
print(type(lis))
print(lis[0])  #Accesing the ith element in the list
lis[0] = 5  #Changing the ith element of the list
print(lis[0])  
lis
```

    <class 'list'>
    1
    5
    




    [5, 2, 3]




```python
print(lis[:]) #It will print the whole list
```

    [5, 2, 3, 5, 9, 10]
    


```python
print(lis[1:2])  #It will print the index 1 to 1
```

    [2]
    


```python
print(lis[0:10])  #Will print from index 0 to 10 (as the size was 3 it will print till last element)
```

    [5, 2, 3, 5, 9, 10]
    


```python
lis.insert(1,20)  #Will insert 20 at index 1
lis
```




    [5, 20, 20, 2, 3, 5, 9, 10]




```python
lis.insert(20,5) #As the size limit is exceeding it will automatically add at the end
lis
```




    [5, 20, 20, 2, 3, 5, 9, 10, 5]




```python
lis.append([9,10,11]) #Appends
lis
```




    [5, 20, 2, 3, 5, [9, 10, 11]]




```python
lis.extend([9,10,11])  #Append and extend are different
lis
```




    [5, 20, 2, 3, 5, [9, 10, 11], 9, 10, 11]




```python
lis.remove(20)  #Removes the number in argument (If multiple present removes the first one)
lis
```




    [5, 2, 3, 5, [9, 10, 11], 9, 10, 11]




```python
lis.pop()  #Pops the last element (Returns it)
lis
```




    [5, 2, 3, 5, [9, 10, 11], 9, 10]




```python
lis.pop(4)  #Will pop from index 4
lis
```




    [5, 2, 3, 5, 9, 10]




```python
print(type(lis[0]))
print(type(lis))
```

    <class 'int'>
    <class 'list'>
    

Lists actually stores the references of the data. Thus we can store multiple type of data there. Another important point is that lists store those references continuously.

How continuity is maintained?
The list copies itself with double size at another available space in appending condition.


## Looping on the list


```python
li = [1,2,"Rohan",9,10]
for i in range(0,len(li),1):
    print(li[i])
print("Length of this list is",len(li))
```

    1
    2
    Rohan
    9
    10
    Length of this list is 5
    


```python
for i in li: #List can be accessed like this also
    print(i)
```

    1
    2
    Rohan
    9
    10
    


```python
for i in li[2:]: #started from index 2
    print(i)
```

    Rohan
    9
    10
    

## Negative indexing and sequencing


```python
li = [1,2,3,4,5]
m = -3
print(li[m])
print(li[-1]) #Negative indexing means starting from the last of list
```

    3
    5
    


```python
print(li[1:4:2]) #list[start:end:step] 
#by default
```

    [2, 4]
    


```python
print(li[1:20:2]) #Will go till length of list if end > length
print(li[1::2]) #dafault value of end
print(li[:3])
print(li[-1:])
print(li[-1::-1])
```

    [2, 4]
    [2, 4]
    [1, 2, 3]
    [5]
    [5, 4, 3, 2, 1]
    

Dafault values are : start = 0, end = length, step = 1

## Taking inputs in a List


```python
#Line seperated input
n = int(input())
li = []
for i in range(0,5,1):
    li.append(int(input()))
print(li)
```

    5
    1
    2
    3
    4
    5
    [1, 2, 3, 4, 5]
    


```python
#Space seperated input
n = int(input())
li = []
str = input()
str = str.split(' ')
for ele in str:
    li.append(int(ele))
print(li)
```

    5
    1 2 3 4 5
    [1, 2, 3, 4, 5]
    


```python
str = input()
str2 = str.split(' ') #Splits the list on basis of space
print(str2)
```

    1 2 3 4 5
    ['1', '2', '3', '4', '5']
    


```python
#Space seperated input part 2
n = int(input())
li = [int(x) for x in input().split()]
print(li)
```

    5
    1 2 3 4 5
    [1, 2, 3, 4, 5]
    

## Concept of Mutable and Immutable

References are changes when we change variable and not the value. This concept is concept of immutable
If we change in one list that will reflet in other list if both list are pointing to same.This concept is concept of mutable


```python
#Mutable concept
li = [1,2,3,4]
li2 = li
li2[0] = 5
print(li) #changed in li2 and li also got changed
print(li2)
```

    [5, 2, 3, 4]
    [5, 2, 3, 4]
    


```python
#Immutable concept
li = [1,2,3,4]
print(id(li))
li = [3,3,3,4]
print(id(li))
```

    2399005431488
    2399005355136
    

## Passing variable to functions


```python
def increment(a):
    a = a + 1
    return a
a = 2
increment(a)  #The variable value didn't changed here (Variables are Immutable)
print(a)
```

    2
    

## Passing List to functions


```python
def increment(li):
    li[0] = li[0] + 1
    return 
li = [1,2,3,4]
increment(li)  #The list value got changed (Lists are mutable)
print(li)
```

    [2, 2, 3, 4]
    

## Swapping


```python
a = 10
b = 12
a,b = b,a
print(a)
print(b)
```

    12
    10
    

## Binary Search


```python
def binarysearch(st,en,li,x):
    while(st<en):
        mid = (st+en)//2
        if(li[mid]==x):
            return mid
        elif(x<li[mid]):
            en = mid - 1
        else:
            st = mid + 1
    return -1
n = int(input())
li = [int(x) for x in input().split()]
li.sort()
x = int(input())
st = 0
en = n - 1
index = binarysearch(st,en,li,x)
print(index)
```

    9
    1 3 8 9 11 13 70 89 98
    200
    -1
    

## Selection Sort


```python
n = int(input())
li = [int(x) for x in input().split()]
minind = 0
i = 0
j = i + 1
while(i<n):
    j = i + 1
    minind = i
    while(j<n):
        if(li[j]<li[minind]):
            minind = j
        j = j + 1
    li[i],li[minind] = li[minind],li[i]
    i = i + 1
print(li)
```

    7
    1 5 3 7 2 6 0
    [0, 1, 2, 3, 5, 6, 7]
    

## Bubble Sort


```python
n = int(input())
li = [int(x) for x in input().split()]
i = 0
for i in range(0,n,1):
    for j in range(0,n-i-1,1):
        if(li[j]>li[j+1]):
            li[j],li[j+1] = li[j+1],li[j]
print(li)
```

    7
    5 3 6 7 1 0 3
    [0, 1, 3, 3, 5, 6, 7]
    

## Insertion Sort


```python
n = int(input())
li = [int(x) for x in input().split()]
for i in range(0,n,1):
    j = i
    while(j-1>=0 and li[j-1]>li[j]):
        li[j],li[j-1] = li[j-1],li[j]
        j = j - 1
print(li)
```

    7
    7 6 5 4 3 2 1
    [1, 2, 3, 4, 5, 6, 7]
    

## Merge Two Sorted Arrays


```python
n = int(input())
li = [int(x) for x in input().split()]
m = int(input())
li2 = [int(x) for x in input().split()]
i = 0
j = 0
ans = []
while(i<n and j<m):
    if(li[i]<li2[j]):
        ans.append(li[i])
        i = i + 1
    else:
        ans.append(li2[j])
        j = j + 1
while(i<n):
    ans.append(li[i])
    i = i + 1
while(j<m):
    ans.append(li2[j])
    j = j + 1
print(ans)
```

    5
    1 3 5 6 7
    3
    1 2 6
    [1, 1, 2, 3, 5, 6, 6, 7]
    

## Strings

Strings is a sequence of unicodes



```python
s1 = 'Pranjal'
s2 = "Pranjal"
s3 = '''Pranjal'''
s4 = '''Here 
is our                   
multiline code'''  #Triple quotes are used for multiline strings
print(s1,s2,s3,s4)
```

    Pranjal Pranjal Pranjal Here 
    is our                   
    multiline code
    


```python
print(s1[-1],' ',s2[0])
```

    l   P
    


```python
a = 'Pranjal'
#a[0] = 'A' is not allowed
#strings are immutable
print(a)
```

    Pranjal
    


```python
s1 = 'Pranjal '
s2 = 'in the sky'
s1 += s2
print(s1)
```

    Pranjal in the sky
    


```python
a = 'Blue'
a *= 3
print(a)
```

    BlueBlueBlue
    

## Slicing of string


```python
str = "Pranjal"
print(str[0:4:1])
print(str[4:20:1])
```

    Pran
    jal
    


```python
str = "Pranjal is in the sky"
print(str[::-1])
```

    yks eht ni si lajnarP
    

## Iterating on string


```python
str = "Pranjal"
for i in range(0,len(str),1):
    print(str[i])
```

    P
    r
    a
    n
    j
    a
    l
    


```python
for i in str:
    print(i)
```

    P
    r
    a
    n
    j
    a
    l
    

## In and Not In Operation


```python
str = 'Hello'
if 'Hell' in str:
    print("Yes, it is a substring")
else:
    print("No, not a substring")
if 'Heo' not in str:
    print("No, it is not there")
else:
    print("It is there")
```

    Yes, it is a substring
    No, it is not there
    

## Comparison operators on string

= <= >= == < > !=


```python
a = 'Pranjal' == 'Pranjal'
print(a)
```

    True
    

 ## Operations on String


```python
#split
str = "Pranjal is in the sky"
li = str.split(' ',2) #If I am passing 2 then it will split into 2 items
print(li)
```

    ['Pranjal', 'is', 'in the sky']
    


```python
#replace
str = "Pranjal is in the sky"
str = str.replace('sky','ground')
str = str.replace('grass','leash')
str2 = "Pranjal Pranjal Pranjal"
str2 = str2.replace('Pranjal','Prmnj',2) #by default it will change only one
print(str)
print(str2)
```

    Pranjal is in the ground
    Prmnj Prmnj Pranjal
    


```python
#find
str = "My name is Pranjal"
index = str.find("na")
print(index)
index = str.find("Nae")
print(index)
index = str.find("na",3,8)  #I am trying to find na in between index 3 to 8
print(index)
```

    3
    -1
    3
    


```python
#lower and upper
str = "PranjaL"
str = str.lower()
print(str)
str = str.upper()
print(str)
```

    pranjal
    PRANJAL
    


```python
#starts with
str = "My name"
ans = str.startswith("M")
print(ans)
ans = str.startswith("My na")
print(ans)
ans = str.startswith("me",5,8)
print(ans)
```

    True
    True
    True
    

## Replacing in string


```python
#Compress the string
def compress(strg):
    count = [0]*256
    ans = ''
    currentcharcount = 1
    ans += strg[0]
    for i in range(1,len(strg)):
        if(strg[i]==strg[i-1]):
            currentcharcount+=1
        else:
            if(currentcharcount>1):
                ans+=str(currentcharcount)
                currentcharcount = 1
            ans+=strg[i]
    if(currentcharcount>1):
        ans+=str(currentcharcount)
    return ans
strg = input()
strg = compress(strg)
print(strg)
```

    aaabbccdsa
    a3b2c2dsa
    

## Two Dimensional List


```python
#lists are mutable
li = [[1,2,3,4],[2,3,4,5],[3,4,5,6],[4,5,6,7]]
print(li[3][0])
li[3][0] = 5
print(type(li))
print(li)
```

    4
    <class 'list'>
    [[1, 2, 3, 4], [2, 3, 4, 5], [3, 4, 5, 6], [5, 5, 6, 7]]
    

li stores address of an array. That array stores addresses of another lists. For example, li[0] stores address of li[0][0]. In this manner it works.


```python
li = [[1,2,3,4],[2,3,4,5],[3,4,5,6],[4,5,6,7]]
print(id(li))
print(id(li[0]))
print(id(li[0][0]))
li[1] = "Pranjal"
print(li) #Now this is not a 2D list
```

    2729917160128
    2729917159104
    140703473346352
    [[1, 2, 3, 4], 'Pranjal', [3, 4, 5, 6], [4, 5, 6, 7]]
    

##  Jagged Lists


```python
#Not the size of all lists are same
li = [[1,2,3,4,5],[1,2],[1,2,3,4]]
print(li)
print(type(li))
```

    [[1, 2, 3, 4, 5], [1, 2], [1, 2, 3, 4]]
    <class 'list'>
    

## List Comprehension


```python
li = [1,2,3,4,6,7,4,2,10]
li_new = [ele**2 for ele in li]  #They say it power of Python
print(li_new)
```

    [1, 4, 9, 16, 36, 49, 16, 4, 100]
    


```python
li_new = [ele**2 for ele in li if ele%2==0]  #li[output for (condition)]
print(li_new)
```

    [4, 16, 36, 16, 4, 100]
    


```python
li1 = [2,3,5,7,8,4,2]
li2 = [6,1,6,2,4,9]
li_new = [ele for ele in li1 for ele2 in li2 if ele==ele2]
print(li_new)
```

    [2, 4, 2]
    

li = [output forloops condition]


```python
li = [1,2,3,4,5,6,7,10]
li_new = [ele if ele%2==1 else ele**2 for ele in li]
print(li_new)
```

    [1, 4, 3, 16, 5, 36, 7, 100]
    


```python
str = "Pranjal"
li = [ord(ele) for ele in str]
print(li)
```

    [80, 114, 97, 110, 106, 97, 108]
    


```python
li = [[1,2,3,4,5],[1,2],[1,2,3,4]]
print(len(li))
li_new = [[ele if ele%2==1 else ele**2 for ele in s] for s in li]
print(li_new)
```

    3
    [[1, 4, 3, 16, 5], [1, 4], [1, 4, 3, 16]]
    

## Taking input of 2-D Lists


```python
n,m = [int(x) for x in input().split()]
li = [[int(x) for x in input().split()] for i in range(n)]
print(li)
```

    3 4
    1 2 3 4
    2 3 4 5
    3 4 5 6
    [[1, 2, 3, 4], [2, 3, 4, 5], [3, 4, 5, 6]]
    

Taking input of Jagged lists


```python
n = int(input())
li = [[int(x) for x in input().split()] for i in range(n)]
print(li)
```

    3
    1 2 3 4
    1 2
    1 2 3 4 5 6
    [[1, 2, 3, 4], [1, 2], [1, 2, 3, 4, 5, 6]]
    

Taking inputs in different manner


```python
#3 4
# 1 2 3 4 5 6 7 8 9 10 11 12
n,m = [int(x) for x in input().split()]
splitedstring = input().split()
arr = [[int(splitedstring[m*i+j]) for j in range(m)]for i in range(n)]
print(arr)
```

    3 4
    1 2 3 4 5 6 7 8 9 10 11 12
    [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]]
    


```python
#3 4 1 2 3 4 5 6 7 8 9 10 11 12
str = input().split()
n,m = int(str[0]),int(str[1])
b = str[2:]
arr = [[int(b[m*i+j]) for j in range(m)] for i in range(n)]
print(arr)
```

    3 4 1 2 3 4 5 6 7 8 9 10 11 12
    [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]]
    

## Iterating on 2-D Lists


```python
str = input().split()
n,m = int(str[0]),int(str[1])
b = str[2:]
arr = [[int(b[m*i+j]) for j in range(m)] for i in range(n)]
print(arr)
```

    3 4 1 2 3 4 5 6 7 8 9 10 11 12
    [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]]
    

## Join 


```python
strg = "ab".join("abcd") #Joins ab in end of each element besides the ending one
print(strg)
```

    aabbabcabd
    


```python
li = [[1,2,3,4],[2,3,4],[1,2]]
for row in li:
    p = ' '.join(str(ele) for ele in row)
    print(p)
#1 2 3 4
#2 3 4
#1 2
```

## Tuples


```python
#Tuples are similar thing to lists declared with a round brackets
a = [1,2]
print(type(a))
b = (1,2)
print(type(b))
```

    <class 'list'>
    <class 'tuple'>
    


```python
e = (1,3,4,6,7,8,10,9)
print(e)
print(e[::-1])
print(e[3:7:2])
del e #Deletes the tuple
```

    (1, 3, 4, 6, 7, 8, 10, 9)
    (9, 10, 8, 7, 6, 4, 3, 1)
    (6, 8)
    

Difference between tuples and lists: Lists are mutable while tuples are immutable


```python
a = (1,2,3)
for i in a:
    print(i)
2 in a #Finding an element in tuple
print(len(a))
b = 4,5  #It is also a tuple
c = a + b
print(c)
d = (a,b)
print(d)
```

    1
    2
    3
    3
    (1, 2, 3, 4, 5)
    ((1, 2, 3), (4, 5))
    


```python
print(min(a))
print(max(b))
```

    1
    5
    


```python
a = (1,2.2) #but min(a) where a = (1,2,'Sep') is not allowed
print(min(a))
```

    1
    

## Passing variable length input and output to function


```python
def sum(a,b,*more):
    ans = a + b
    for ele in more:
        ans += ele
    return ans
sum(1,2,3,4,5,6,7)
```




    28




```python
def sum_diff(a,b):
    return a+b,a-b
print(sum_diff(3,2)) #Is outputing a tuple
```

    (5, 1)
    

## Dictionary


```python
a = {}
print(a)
print(type(a))
a = {"the":3,100:2,2.2:5}
for ele in a:
    print(ele)
print(type(a))
```

    {}
    <class 'dict'>
    the
    100
    2.2
    <class 'dict'>
    


```python
b = dict([(1,4),('the',5)])
print(b)
c = a.copy()
print(c)
d = dict.fromkeys(['abc',32,4])
print(d)
```

    {1: 4, 'the': 5}
    {'the': 3, 100: 2, 2.2: 5}
    {'abc': None, 32: None, 4: None}
    

Dictionaries are mutable

## Accesing a dictionary


```python
a = {1:2,3:4,"list":[1,23],"dict":{1:2}}
print(a['list'])
print(a[1])
print(a.get('dict'))
print(a.get('this will not give error'))
print(a.get('you can return something else',-1))
```

    [1, 23]
    2
    {1: 2}
    None
    -1
    


```python
a.keys()
```




    dict_keys([1, 3, 'list', 'dict'])




```python
a.values()
```




    dict_values([2, 4, [1, 23], {1: 2}])




```python
a.items()
```




    dict_items([(1, 2), (3, 4), ('list', [1, 23]), ('dict', {1: 2})])




```python
for ele in a:
    print(ele,a[ele])
```

    1 2
    3 4
    list [1, 23]
    dict {1: 2}
    


```python
for i in a.values():
    print(i)
```

    2
    4
    [1, 23]
    {1: 2}
    


```python
for i in a.keys():
    print(i)
```

    1
    3
    list
    dict
    


```python
print('list' in a)
print(2 in a)
```

    True
    False
    

## Updating data in dictionary


```python
a = {1:2,3:4,"list":[1,23],"dict":{1:2}}
a[9] = 1
#We added an element
```




    {1: 2, 3: 4, 'list': [1, 23], 'dict': {1: 2}, 9: 1}




```python
a[1] = 10
#We updated data
```




    {1: 10, 3: 4, 'list': [1, 23], 'dict': {1: 2}, 9: 1}




```python
b = {3:5,'the':1000}
a.update(b)
print(a)
#We can update one dictionary with help of other
```

    {1: 10, 3: 5, 'list': [1, 23], 'dict': {1: 2}, 9: 1, 'the': 1000}
    


```python
a.pop('the')
print(a)
```

    {3: 5, 'list': [1, 23], 'dict': {1: 2}, 9: 1}
    


```python
del a[3]
print(a)
```

    {'list': [1, 23], 'dict': {1: 2}, 9: 1}
    


```python
del a
#Dictionary is gone forever
```

## Sets


```python
a = {'apple','mango',5,2.2,5} #Does not allow duplicates
print(type(a))
print(a)
```

    <class 'set'>
    {2.2, 'mango', 5, 'apple'}
    


```python
print('apple' in a)
len(a)
```

    True
    




    4




```python
a.add('temp') #Adding elements in a
print(a)
b = {'abc',78}
a.update(b)
print(a)
```

    {2.2, 'mango', 5, 'apple', 'temp'}
    {2.2, 'mango', 5, 'abc', 78, 'apple', 'temp'}
    


```python
a.remove('abc')  #The value which is not there is not allowed
a.remove(78)
print(a)
a.discard('apple')  #The value which is not there is allowed
a.discard("plum")
print(a)
```

    {2.2, 'mango', 5, 'apple', 'temp'}
    {2.2, 'mango', 5, 'temp'}
    


```python
a.pop()
```




    2.2




```python
a.clear()
print(a)
del a
```

    set()
    

## Functions related to sets


```python
a = {1,2,3,4}
b = {3,4,5,6}
a.intersection(b)
```




    {3, 4}




```python
a.union(b)
```




    {1, 2, 3, 4, 5, 6}




```python
print(a.difference(b))
print(b.difference(a))
```

    {1, 2}
    {5, 6}
    


```python
print(a.symmetric_difference(b))
print(b.symmetric_difference(a))
```

    {1, 2, 5, 6}
    {1, 2, 5, 6}
    


```python
a.intersection_update(b)
print(a)
```

    {3, 4}
    


```python
a.issubset(b)
```




    False




```python
a.isdisjoint(b) #They have something in common
```




    False



# THE END
