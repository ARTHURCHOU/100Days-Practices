# Fourth Day to follow the 'Python-100-Days' practice

**Practice1**

Check if the input int is a prime:

    from math import sqrt

    num=int(input('Please input an int: '))
    end=int(sqrt(num))
    is_prime = True
    for x in range(2, end+1):
        if num % x == 0:
            is_prime = False
            break
    if is_prime and num != 1:
        print('It is a prime')
    else:
        print('It is not a prime')

**Result:**

    Please input an int: 3
    It is a prime

    Please input an int: 4
    It is not a prime

**Practice2**

Calculate the Highest Common Factor and the Least Common Multiple of the two input ints.

    from math import sqrt

    x1=int(input('Please input the first int: '))
    x2=int(input('Please input the second int: '))
    x_max=max(x1,x2)
    for i in range (x_max,1,-1):
        if x1 % i ==0 and x2 % i == 0:
            print('the Highest Common Factor of %d and %d is %d' %(x1, x2, i))
            print('the Least Common Multiple of %d and %d is %d' %(x1, x2, x1*x2//i))

**Result:**

    Please input the first int: 4
    Please input the second int: 6
    the Highest Common Factor of 4 and 6 is 2
    the Least Common Multiple of 4 and 6 is 12

**Practice3**

    for i in range(1,6):
        print('*' * i)

    for i in range(1,6):
        print(' ' * (5-i) + '*' * i)

    for i in range(1,6):
        print(' ' * (5-i) + '*' * (2*i-1))

**Better Answer:**

    row = int(input('Please input the raw: '))
for i in range(row):
    for _ in range(i + 1):
        print('*', end='')
    print()


for i in range(row):
    for j in range(row):
        if j < row - i - 1:
            print(' ', end='')
        else:
            print('*', end='')
    print()

for i in range(row):
    for _ in range(row - i - 1):
        print(' ', end='')
    for _ in range(2 * i + 1):
        print('*', end='')
    print()

**Result:**

    Please input the raw: 5
    *
    **
    ***
    ****
    *****
        *
       **
      ***
     ****
    *****
        *
       ***
      *****
     *******
    *********