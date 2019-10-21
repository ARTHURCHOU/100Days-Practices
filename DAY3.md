# Third Day to follow the 'Python-100-Days' practice
**Practice1**

Convert in and cm to each other:

    value=float(input('Please input the longth'))
    unit=input('Please input unit')
    if unit=='in':
        print('%f in = %f cm' %(value, value * 2.54))
    elif unit=='cm':
        print('%f cm = %f in' %(value, value / 2.54))
    else:
        print('Please input correct unit')

**Result:**

    Please input the longth10
    Please input unitcm
    10.000000 cm = 3.937008 in

    Please input the longth10
    Please input unitin
    10.000000 in = 25.400000 cm

    Please input the longth10
    Please input unitm
    Please input correct unit

**Practice2**

Convert score to grade:

    score=float(input('Please input the score: '))
    if score >= 90:
        grade='A'
    elif score >= 80:
        grade='B'
    elif score >= 70:
        grade='C'
    elif score >= 60:
        grade='D'
    else:
        grade='E'
    print('The corresponding grade is: ' + grade)

**Result:**

    Please input the score: 67
    The corresponding grade is: D

**Practice3**

Input 3 value, if they can form a triangle, calculate the perimeter and area:

    a=float(input('a= '))
    b=float(input('b= '))
    c=float(input('c= '))

    if a+b>c and a+c>b and b+c>a:
        print('Perimeter is %f' %(a+b+c))
        p=(a+b+c)/2
        area=(p*(p-a)*(p-b)*(p-c))**0.5
        print('Area is %f' % area)
    else:
        print('It can not form a triangle')

**Result:**

    a= 1
    b= 1
    c= 1
    Perimeter is 3.000000
    Area is 0.433013

    a= 3
    b= 1
    c= 1
    It can not form a triangle