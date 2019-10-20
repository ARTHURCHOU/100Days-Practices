# Second Day to follow the 'Python-100-Days' practice
**Practice1**

Transport degree Fahrenheit to degree Celsius

    f = float(input('Please input degree Fahrenheit:'))
    c = (f-32)/1.8
    print('%.1f degree Fahrenheit = %.1f degree Celsius' %(f, c))

**Result:**

    Please input degree Fahrenheit:100
    100.0 degree Fahrenheit = 37.8 degree Celsius

**Practice2**

Calculate the perimeter and area from the import radius

    import math

    radius = float(input('Please import the radius'))
    perimeter = 2*math.pi*radius
    area = math.pi * radius * radius
    print('Perimeter = %.2f' % perimeter)
    print('Area = %.2f' % area)

**Result:**

    Please import the radius 3
    Perimeter = 18.85
    Area = 28.27

**Practice3**

Determine whether the year entered is a leap year

    year = int(input('Please input the year:'))

    is_leap = (year % 4 == 0 and year % 100 != 0 ) or year % 400 == 0
    print(is_leap)

**Result**

    Please input the year:2019
    False
    Please input the year:2008
    True
    Please input the year:2000
    True
    Please input the year:1900
    False