# lab2
Лабораторная 2 Веб-программирование

1. Написать функцию, которая на вход принимает int и возвращает true или false
в зависимости является ли это число палиндром. Число является
палиндромом, если оно читается справа налево и слева направо одинаково (25)

def palindrom(k):
    num = int(input("Введите число:")) 
    temp = num
    rev = 0 
    while(num > 0):
        dig = num % 10 
        rev = rev * 10 + dig 
        num = num // 10
        if(temp == rev):
            print("Введенное число является палиндромом")
            else:
                print("Введенное число НЕ является палиндромом")

2. Написать функцию, которая принимает на вход список из положительных
целочисленных элементов и возвращает три списка: (25)

a. в первом - числа, которые делятся на 2
b. во втором - числа, которые делятся на 3
c. с третьем - числа, которые делятся на 5

def delenie235(lst):
    tw = []
    th = []
    f = []
    for i in lst:
        if i%2 == 0:
            tw.append(i)
        if i%3 == 0:
            th.append(i)
        if i%5 == 0:
            f.append(i)
            return tw, th, f
        lst = []
        for e in input("Введите числа:").split():
            lst.append(int(e))
            a = (d(lst))
            for i in a:
                print (i)

3. Написать функцию, принимающую на вход int, и число, обратное этому int (25)

def perevorot(l):
    n1 = int(input("Введите целое число: "))
    n2 = 0
while n1 > 0:
    d = n1 % 10
    n1 = n1 // 10
    n2 = n2 * 10
    n2 = n2 + d
print('Обратное ему число:', n2)

4. Написать функцию, которая будет расчитывать квадратный корень n-ой
степени методом Ньютона

def sqrt(x):
    def sqrtIter(guess):
        if goodEnaugh(guess):
            return guess
        else:
            return sqrtIter(improve(guess))
    def improve(guess):
        return average(guess, x/guess)
    def average(x, y):
        return (x+y)/2
    def goodEnaugh(guess):
        if(abs(guess**2-x)<0.001):
            return 1
        else:
            return 0
    return sqrtIter(1.0)

5. Написать функцию, принимающую 1 аргумент — число от 0 до 100000, и
возвращающую true, если оно простое, false если нет. (35)

def trufal(n):
   if n < 2:
       return False
   if n == 2:
       return True
   limit = n**(1/2)
   i = 2
   while i <= limit:
       if n % i == 0:
           return False
       i += 1
   return True
print(trufal(int(input("Число: "))))
