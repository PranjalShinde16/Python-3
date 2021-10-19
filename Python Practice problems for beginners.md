Calculate Simple Interest


```python
p = 100
r = 12
t = 2
si = (p * r * t)/100
print(si)
```

    24.0
    

Farenheit to Celcius conversion


```python
f = 100
c = (f-32)*(5/9)
print(c)
```

    37.77777777777778
    

Calculate SI by taking input of p r t from user


```python
print("Give the value for p")
p = int(input())
print("Give the value for r")
r = int(input())
print("Give the value for t")
t = int(input())
si = (p*r*t)/100
print("The value of SI is ", si)
```

    Give the value for p
    20
    Give the value for r
    10
    Give the value for t
    2
    The value of SI is  4.0
    

Conversion from F to C by taking input


```python
print("Give the value of F to be converted")
f = float(input())
c = (f-32)*(5/9)
print("The converted value in C is ", c," Celcius")
```

    Give the value of F to be converted
    100
    The converted value in C is  37.77777777777778  Celcius
    

Average of three marks


```python
a = int(input())
b = int(input())
c = int(input())
print((a+b+c)/3)
```

    10
    20
    30
    20.0
    

Check if a number is even or odd


```python
n = int(input())
n = n%2
if (n==0):
    print("n is even")
else:
    print("n is odd")
```

    1
    n is odd
    

Print if both are greater than 10


```python
a = int(input())
b = int(input())
if (a>10 and b>10):
    print("Yes")
else:
    print("No")
```

    34
    50
    Yes
    

See if given number is 7 or not


```python
a = float(input())
if (a==7):
    print("Yes")
else:
    print("No")
```

    7.00
    Yes
    

Write all numbers till n, starting from 1


```python
n = int(input())
l = 0
while l<=n:
    print(l)
    l = l + 1
```

    3
    0
    1
    2
    3
    

Code to find if a number is a prime number


```python
n = int(input())
count = 0
num = 1
while (num<=n):
    if (n%num==0):
        count = count + 1
    num = num +1
if (count>2):
    print("Number is not prime")
elif (count==1):
    print("Number is not prime nor composite")
else:
    print("Number is prime")
```

    41
    Number is prime
    

Print a pxp matrix


```python
n = int(input())
i = 0
j = 0
while(i<n):
    j = 0
    while(j<n):
        print("*",end='')
        j = j + 1
    print()
    i = i + 1
```

    3
    ***
    ***
    ***
    

Square pattern
1111
2222
3333
4444


```python
n = int(input())
i = 1
j = 0
while (i<=n):
    j = 0
    while (j<n):
        print(i,end='')
        j = j+1
    print()
    i = i + 1
```

    3
    111
    222
    333
    

Square pattern
1234
1234
1234


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = 1
    while(j<=n):
        print(j,end='')
        j = j+1
    print()
    i = i + 1
```

    3
    123
    123
    123
    

Square pattern
4321
4321
4321
4321


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = n
    while(j>0):
        print(j,end='')
        j = j - 1
    print()
    i = i + 1
```

    3
    321
    321
    321
    

Triangular pattern
1
12
123
1234


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = 1
    while(j<=i):
        print(j,end='')
        j = j + 1
    print()
    i = i + 1
```

    3
    1
    12
    123
    

Triangular pattern
1
23
345
4567


```python
n = int(input())
i = 1
j = 1
k = 1
while(i<=n):
    j = i
    p = 1
    while(p<=i):
        print(j,end='')
        j = j + 1
        p = p + 1
    print()
    i = i + 1
```

    3
    1
    23
    345
    

Triangular pattern
1
23
456
7890


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    p = 1
    while(p<=i):
        print(j,end='')
        j = j + 1
        p = p + 1
    print()
    i = i + 1
```

    3
    1
    23
    456
    

Character pattern 
ABCD
ABCD
ABCD
ABCD


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = 1
    a = 'A'
    while(j<=n):
        print(a,end='')
        a = chr( ord(a) + 1 )
        j = j + 1
    print()
    i = i + 1
```

    3
    ABC
    ABC
    ABC
    

Character pattern
ABCD
BCDE
CDEF
DEFG


```python
n = int(input())
i = 1
j = 1
a = 'A'
while(i<=n):
    a = 'A'
    a = chr( ord(a) + i - 1 )
    j = 1
    while(j<=n):
        print(a,end='')
        a = chr( ord(a) + 1 )
        j = j + 1
    print()
    i = i + 1
```

    3
    ABC
    BCD
    CDE
    

Inverted Triangle
****
***
**
*


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = n - i + 1
    while(j>0):
        print('*',end='')
        j = j - 1
    print()
    i = i + 1
```

    3
    ***
    **
    *
    

Inverted Triangle
1111
222
33
4


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = n - i + 1
    while(j>0):
        print(i,end='')
        j = j - 1
    print()
    i = i + 1
```

    3
    111
    22
    3
    

Reversed triangle
   *
  **
 ***
****


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = 1
    while(j<=n-i):
        print(' ',end='')
        j = j + 1
    while(j<=n):
        print('*',end='')
        j = j + 1
    print()
    i = i + 1
```

    3
      *
     **
    ***
    

Reversed Triangle
   1
  12
 123
1234


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = 1
    p = 1
    while(j<=n-i):
        print(' ',end='')
        j = j + 1
    while(j<=n):
        print(p,end='')
        j = j + 1
        p = p + 1
    print()
    i = i + 1
```

    3
      1
     12
    123
    

Isosceles Pattern
   1   
  121
 12321
1234321


```python
n = int(input())
i = 1
j = 1
p = 1
while(i<=n):
    j = 1
    while(j<=n-i):
        print(' ',end='')
        j = j + 1
    j = 1
    while(j<=p):
        print(j,end='')
        j = j + 1
    j = j - 2
    while(j>=1):
        print(j,end='')
        j = j - 1
    p = p + 1
    print()
    i = i + 1
```

    3
      1
     121
    12321
    

Isosceles Pattern
   1
  232
 34543
4567654


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = 1
    while(j<=n-i):
        print(' ',end='')
        j = j + 1
    j = i
    while(j<=(i*2)-1):
        print(j,end='')
        j = j + 1
    j = j - 2
    while(j>=i):
        print(j,end='')
        j = j - 1
    print()
    i = i + 1
```

    3
      1
     232
    34543
    

Diamond Pattern
   *
  ***
 *****
*******
 *****
  ***
   *


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = 1
    while(j<=n-i):
        print(' ',end='')
        j = j + 1
    p = (2*i)-1
    j = 1
    while(j<=p):
        print('*',end='')
        j = j + 1
    print()
    i = i + 1
i = (n - 1)
while(i>0):
    j = 1
    while(j<=n-i):
        print(' ',end='')
        j = j + 1
    p = (i*2) - 1
    j = 1
    while(j<=p):
        print('*',end='')
        j = j + 1
    print()
    i = i - 1
```

    3
      *
     ***
    *****
     ***
      *
    

Arrow Pattern
*
 * *
  * * *
   * * * * 
  * * *
 * *
*


```python
n = int(input())
i = 1
j = 1
while(i<=n):
    j = 1
    while(j<i):
        print(' ',end='')
        j = j + 1
    j = 1
    while(j<=i):
        print('* ',end='')
        j = j + 1
    print()
    i = i + 1
i = n - 1
while(i>0):
    j = 1
    while(j<i):
        print(' ',end='')
        j = j + 1
    j = 1
    while(j<=i):
        print('* ',end='')
        j = j + 1
    print()
    i = i - 1
```

    3
    * 
     * * 
      * * * 
     * * 
    * 
    

Print all multiples of 3 from a to b


```python
a = int(input())
b = int(input())
for i in range(a,b+1,1):
    if(i%3==0):
        print(i," ",end='')
```

    1
    5
    3  

Find if a number is prime or not using for loop


```python
n = int(input())
flag = True
for i in range(2,n,1):
    if(n%i==0):
        print("number is not prime")
        flag = False
if(flag==True):
    print("number is a prime number")
```

    41
    number is a prime number
    

   1
  232
 34543
4567654


```python
n = int(input())
for i in range(1,n+1,1):
    for j in range(1,n-i+1,1):
        print(' ',end='')
    for j in range(i,(2*i),1):
        print(j,end='')
    for j in range((2*i)-2,i-1,-1):
        print(j,end='')
    print()
```

    3
      1
     232
    34543
    

Function to determine if a number is prime or not


```python
def isPrime(n):
    for i in range(2,n,1):
        if(n%i==0):
            break
    else:
        return True
    return False
n = int(input())
b = isPrime(n)
print(b)
```

    2
    True
    

Print all prime numbers from 2 to n


```python
def isprime(n):
    for i in range(2,n,1):
        if(n%i==0):
            break
    else:
        return True
    return False
def printprime(n):
    for i in range(2,n+1,1):
        p = isprime(i)
        if p:
            print(i)
n = int(input())
printprime(n)
```

    10
    2
    3
    5
    7
    

Linear search


```python
n = int(input())
li = [int(x) for x in input().split()]
k = int(input())
for i in range(0,n,1):
    if(li[i]==k):
        print(i)
        break
else:
    print(-1)
```

    7
    1 2 3 4 5 6 7
    8
    -1
    

Linear search using Functions


```python
def find(k,li):
    for i in range(0,n,1):
        if(li[i]==k):
            return i
            break
    return -1
n = int(input())
li = [int(x) for x in input().split()]
l = int(input())
index = find(l,li)
print(index)
```

    7
    1 2 3 4 5 6 7
    8
    -1
    

Reversing a list


```python
def reverse(li,k):
    n = k
    n = n//2
    for i in range(0,n,1):
        li[i],li[k-i-1] = li[k-i-1],li[i]
    return li
n = int(input())
li = [int(x) for x in input().split()]
print(li)
reverse(li,n)
print(li)
```

    5
    1 2 3 4 5
    [1, 2, 3, 4, 5]
    [5, 4, 3, 2, 1]
    


```python
li = [1,2,3,4,5,6]
li = li[::-1]
print(li)
```

    [6, 5, 4, 3, 2, 1]
    

Find the unique number 


```python
#O(nlogn) complexity
def solve():
    n = int(input())
    li = [int(x) for x in input().split()]
    li.sort()
    for i in range(1,n-1,1):
        if(li[i]!=li[i+1] and li[i]!=li[i-1]):
            print(li[i])
            break
    else:
        if(n==1):
            print(li[0])
        elif(li[0]!=li[1]):
            print(li[0])
        elif(li[n-1]!=li[n-2]):
            print(li[n-1])
t = int(input())
while t>0:
    solve()
    t = t - 1
```

    2
    5
    1 3 1 3 4
    4
    7
    1 4 5 6 4 5 6
    1
    

A property of XOR is:
    XOR of a number with itself is 0
    XOR of a number with 0 is the number itself


```python
#O(N) complexity
def solve():
    n = int(input())
    li = [int(x) for x in input().split()]
    ans = 0
    for i in li:
        ans = ans ^ i
    print(ans)
t = int(input())
while t>0:
    solve()
    t = t - 1
```

    2
    5
    2 4 7 2 7
    4
    9
    1 3 1 3 6 6 7 10 7
    10
    

Find the number which is duplicate


```python
def findsum(n):
    sum = 0
    for i in range(0,n-1,1):
        sum = sum + i
    return sum
def solve():
    n = int(input())
    li = [int(x) for x in input().split()]
    sum = 0
    for i in range(0,n,1):
        sum = sum + li[i]
    sum2 = findsum(n)
    print(sum - sum2)
t = int(input())
while t>0:
    solve()
    t = t - 1
```

    2
    5
    0 2 1 3 1
    1
    7
    0 3 1 5 4 3 2
    3
    

Find the intersection of arrays


```python
#O(M*N) complexity
def solve():
    n = int(input())
    li1 = [int(x) for x in input().split()]
    m = int(input())
    li2 = [int(x) for x in input().split()]
    for i in range(0,n,1):
        for j in range(0,m,1):
            if(li1[i]==li2[j]):
                print(li1[i],end=' ')
                li1[i] = -1
                li2[j] = -1
                break
t = int(input())
while(t>0):
    solve()
    t = t - 1
```

    1
    4
    2 6 1 2
    5
    1 2 3 4 2
    2 1 2 

Find number of pairs in list which sum up to X


```python
#O(N^2) complexity
def solve():
    n = int(input())
    li = [int(x) for x in input().split()]
    sum = int(input())
    count = 0
    for i in range(0,n,1):
        for j in range(i+1,n,1):
            #print(li[i]," ",li[j])
            if(li[i]+li[j]==sum):
                count = count + 1
    print(count)
t = int(input())
while(t>0):
    solve()
    t = t - 1
```

    2
    9
    1 3 6 2 5 4 3 2 4
    12
    0
    6
    2 8 10 5 -2 5
    10
    2
    

Find numver of triplets adding to X


```python
#O(N^3) complexity
def solve():
    n = int(input())
    li = [int(x) for x in input().split()]
    sum = int(input())
    count = 0
    for i in range(0,n,1):
        for j in range(i+1,n,1):
            for k in range(j+1,n,1):
                #print(li[i]," ",li[j])
                if(li[i]+li[j]+li[k]==sum):
                    count = count + 1
    print(count)
t = int(input())
while(t>0):
    solve()
    t = t - 1
```

    2
    7
    1 2 3 4 5 6 7
    19
    0
    9
    2 -5 8 -6 0 5 10 11 -3
    10
    5
    

Sort an array containing 0 and 1 only in ascending order in O(N)


```python
def solve():
    n = int(input())
    li = [int(x) for x in input().split()]
    i = 0
    j = n-1
    while(i<j):
        while(li[i]==0):
            i = i + 1
        while(li[j]==1):
            j = j - 1
        if(i>=j):
            break
        li[i],li[j] = li[j],li[i]
    print(li)
t = int(input())
while(t>0):
    solve()
    t = t - 1
```

    2
    8
    1 0 1 1 0 1 0 1
    [0, 0, 0, 1, 1, 1, 1, 1]
    5
    0 1 0 1 0
    [0, 0, 0, 1, 1]
    

All zeros at the end


```python
def solve():
    n = int(input())
    li = [int(x) for x in input().split()]
    i = 0
    while(li[i]!=0):
        i = i + 1
    for j in range(i+1,n,1):
        if(li[j]!=0):
            li[j],li[i] = li[i],li[j]
            while(li[i]!=0):
                i = i + 1
    print(li)
t = int(input())
while(t>0):
    solve()
    t = t - 1
```

    1
    5
    9 0 0 8 2
    [9, 8, 2, 0, 0]
    

Rotate the array


```python
def solve():
    n = int(input())
    li = [int(x) for x in input().split()]
    d = int(input())
    ans = []
    for i in range(d,n+d,1):
        ans.append(li[i%n])
    print(ans)
t = int(input())
while(t>0):
    solve()
    t = t - 1
```

    2
    7
    1 2 3 4 5 6 7
    0
    [1, 2, 3, 4, 5, 6, 7]
    4
    1 2 3 4
    3
    [4, 1, 2, 3]
    

Second largest element in the array


```python
INT_MIN = -2147483648
def solve():
    n = int(input())
    li = [int(x) for x in input().split()]
    li.sort()
    if(n<=1 or (li[n-1]==li[n-2] and li[0]==li[n-1])):
        print(INT_MIN)
    else:
        k = n - 2
        while(li[k]==li[k+1]):
            k = k - 1
        print(li[k])
t = int(input())
while(t>0):
    solve()
    t = t - 1
```

    2
    2
    6 6
    -2147483648
    4
    90 8 90 2
    8
    

Replacing a character in string


```python
str1 = input()
str2 = input()
str = input()
str = str.replace(str1,str2)
print(str)
```

    t
    u
    tuminty tiget
    uuminuy uigeu
    

count numbers of vowels,consonants,digits and special characters in a string


```python
def solve(str):
    v = 0
    c = 0
    d = 0
    s = 0
    for char in str:
        char = char.lower()
        if(char<='z' and char>='A'):
            if(char=='a' or char=='e' or char=='i' or char=='o' or char=='u'):
                v = v + 1
            else:
                c = c + 1
        elif(char>='0' and char<='9'):
            d = d + 1
        else:
            s = s + 1
    return v,c,d,s
str = input()
v,c,d,s = solve(str)
print(v,c,d,s)
```

    aajfajeoiuretya87ygg78hahpp;ipjp'jgeriyeg
    14 21 4 2
    

Check Whether the two strings are permutation of each other or not


```python
def permutation(s,s2):
    s = sorted(s)
    s2 = sorted(s2)
    return s==s2
str = input()
str2 = input()
a = permutation(str,str2)
print(a)
```

    abce
    ebac
    True
    

Remove consecutive duplicates


```python
def unique(str):
    ans = ''
    stind = 0
    while(stind<len(str)):
        ans += str[stind]
        nxtsi = stind + 1
        while(nxtsi<len(str) and str[stind]==str[nxtsi]):
            nxtsi+=1
        stind = nxtsi
    return ans
str = input()
str = unique(str)
print(str)
```

    aabbccdaaggttttt
    abcdagt
    

Reverse each word in the sentence


```python
def reve(str):
    li = str.split(' ')
    ans = ''
    for word in li:
        rev = word[::-1]
        #print(rev)
        ans += rev
        ans += ' '
    return ans
str = input()
str = reve(str)
print(str)
```

    Hello! I am AAdil.
    !olleH I ma .lidAA 
    

Remove Character


```python
def remove(str,char):
    ans = ''
    for ele in str:
        if(ele!=char):
            ans+=ele
    return ans
str = input()
char = input()
str = remove(str,char)
print(str)
```

    aabccbaa
    a
    bccb
    

Return the highest occuring character in a string


```python
def occuring(str):
    count = [0] * 256
    for ele in str:
        num = ord(ele)
        count[num]+=1
    max = 0
    for i in range(0,256,1):
        if(count[i]>max):
            max = count[i]
            ans = i
    #print(ans)
    print(chr(ans))
str = input()
occuring(str)
```

    abdefgbabfba
    98
    b
    

Output the square of those numbers who are div by 2 and 3


```python
li = [2,3,4,5,6,7,8,9]
li_new = [ele**2 for ele in li if (ele%2==0 and ele%3==0)]
print(li_new)
```

    [36]
    

Largest column sum


```python
def lar_col_sum(li):
    n = len(li)
    m = len(li[0])
    maxsum = 0
    index = -1
    for i in range(m):
        sum = 0
        for j in range(n):
            sum += li[j][i]
        if(sum>maxsum):
            maxsum = sum
            index = i
    return index
li = [[1,2,3,4],[8,7,6,5],[9,10,11,7]]
lar_col_ind = lar_col_sum(li)
print(lar_col_ind)
```

    2
    

Given a string str print all letters of freq k


```python
str = 'djgjsughahiaugyuibdhsngjnfhbalajkgnflidbnlrhuaiudhfyeapfjpdkjvjisbr'
k = 3
a = {}
for ele in str:
    a[ele] = 0
for ele in str:
    a[ele] += 1
for ele in a:
    if a[ele] == k:
        print(ele)
```

    s
    l
    

Find the sum of all unique numbers


```python
li = [1,2,4,6,5,6,7,4,1,2,4,4]
st = set()
for ele in li:
    st.add(ele)
ans = 0
for ele in st:
    ans += ele
print(ans)
```

    25
    

# THE END
