# Fourth Day to follow the 'Python-100-Days' practice

**Practice1**

Print the first 20 number in fibonacci:

    x1=1
    x2=1
    print(x1)
    print(x2)
    for i in range(18):
        x = x1 + x2
        x1 = x2
        x2 = x
        print(x)

**Result:**

    1
    1
    2
    3
    5
    8
    13
    21
    34
    55
    89
    144
    233
    377
    610
    987
    1597
    2584
    4181
    6765

**Practice2**

Find out the perfect numbers in 10000:

    import math

    for num in range(1, 10000):
        result = 0
        for factor in range(1, int(math.sqrt(num)) + 1):
            if num % factor == 0:
                result += factor
                if factor > 1 and num // factor != factor:
                    result += num // factor
        if result == num:
            print(num)\

**Result:**

    1
    6
    28
    496
    8128

**Practice3**

Print all prime in 100:

    import math

    for i in range(2,100):
        is_prime = True
        for x in range(2, int(math.sqrt(i))+1):
            if i % x == 0:
                is_prime = False
                break
        if is_prime:
            print(i)

**Result:**

    2
    3
    5
    7
    11
    13
    17
    19
    23
    29
    31
    37
    41
    43
    47
    53
    59
    61
    67
    71
    73
    79
    83
    89
    97