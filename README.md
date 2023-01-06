# calculator
simple calculator using lambda function

import sys 
import my_logger
try:
    
    title = ("calculator")
    print(title.center(60,'*'))

    while(True):
        print('**********Operations************')
        print('1]Addition')
        print('2]Substraction')
        print('3]Division')
        print('4]Multiplication')
        print('5]Exit')
        

        print('--'*50)
        choice = int(input("Enter Your Choice [1/2/3/4/5] = "))
        print('--'*50)

        if choice in range(1,5) :
            x = float(input("Enter first no = "))
            y = float(input("Enter second no = "))

            print('--'*50)

        
            if choice == 1:
                addition = lambda x,y : x+y
                print("addition = ",addition(x,y))
            elif choice == 2:
                substraction = lambda x,y : x-y
                print("substraction = ",substraction(x,y))
            elif choice == 3:
                division = lambda x,y : x/y
                print("division = ",division(x,y))
            elif choice == 4:
                multiplication = lambda x,y : x*y
                print("multiplication = ",multiplication(x,y))
        elif choice == 5:
            sys.exit()        
        else:
            print("Enter valid choice")          
except BaseException as ex:
    my_logger.logging(f"error occured = {ex}") 
