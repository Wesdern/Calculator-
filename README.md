# Calculator
from math import pi, sqrt
from random import randint
print('v.3.8.5')
userName=str(input('Enter your name>> '))
def rand(a, b):
    return randint(a, b)
def sqF(x):
    return sqrt(x)
while True:
    print('''╔╔╗║╔║║║╔╗╦╔╗╔╗
║╠╣║║║║║╠╣║║║╠╝
╚║║╚╚╚╝╚║║║╚╝╠╗
''')
    print('MENU:')
    print('Enter "1" to open calculator')
    print('Enter "2" to open PI menu')
    print('Enter "3" to open sqrt menu')
    print('Enter "4" to get random number')
    print('Enter "5" to get random boolean')
    print('Enter "6" to close programm')
    ip=str(input('>> '))
    #Получает пользовательский ввод в МЕНЮ
    try:
#---------------calc----------------------
        if ip=='1':
            num1=int(input('Enter first number>> '))#Получает первое число
            sign=input('enter sign>>  ')#Получает знак
            num2=int(input('Enter second number>> '))#получает второе число
            if sign=='+':#Прибавляет
                print('= '+str(num1+num2))
                input('press Enter  ')
            elif sign=='-':#Вычитает
                print('= '+str(num1-num2))
                input('press Enter  ')
            elif sign=='*':#Умножает
                print('= '+str(num1*num2))
                input('press Enter  ')
            elif sign=='/':#Делит
                print('= '+str(num1/num2))#Выводит ответ в 
                print('= '+str(num1//num2)+'(остаток '+str(num1%num2)+')')#Выводит ответ в int +остаток
                input('press Enter  ')
            else:
                print('Unknow sign, use + - * /')
                input('press Enter  ')
#----------------quit---------------------
        elif ip=='6':
            print('Are you sure y|n')
            su=input('>> ')
            if su == 'y':                
                print('Good bye, '+userName.title()+'...')
                print('Comming back soon!')
                break
            else:
                print('RELOAD')
                input('press Enter ')                                                #----------------boolean-----------------
        elif ip=='5':
            e=rand(1,2)
            if e==1:
                print('>> True')
                input('press Enter ')
            elif e==2:
                print('>> False')
                input('press Enter ')
            else:
                print('Error')
                input('press Enter ')
#----------------sqrt---------------------
        elif ip=='3':
            print('Enter- x')
            ss=int(input('>> '))
            print('= '+str(sqF(ss)))
            input('press Enter ')
#---------------random------------------
        elif ip=='4':
            print('From')
            q=input('>> ')
            print('To')
            w=input('>> ')
            print('= '+str(rand(q, w)))
            input('press Enter ')
#----------------pi-----------------------
        elif ip=='2':
            print('Enter-n: pi*N')
            print('or')
            print('Enter- pi')
            entPi=input('>> ')
            if entPi=='n':
                print('Enter-n(n=?)')
                n=input('>> ')
                print('pi * '+str(n)+' = '+str(pi*n))
                input('press Enter ')
            elif entPi=='pi':
                print('PI= '+str(pi))
                input('press Enter ')
            else:
                print('Unknow put, please repit your put')
                input('press Enter ')
        else:
            print('Unknow put')
            input('press Enter  ')
#----------------error_block--------------
    except ZeroDivisionError:
        print('ZeroDivisionError, please repit your put')
        #Выдаёт программную ошибку при делении на ноль
        input('press Enter  ')
    except:
        print('UNKNOW ERROR, please repit your put')
        #Выдаёт программную ошибку при получении неизвестного исключения
        input('press Enter  ')
