# First-Repository--Password-Checker
Password Strength Verification in Python

          import re

          def main():

                    password= input("Input Desired Password Here:")
                    Y=True #Y is set for True and is a random variable
                    while Y:  #while Y is TRUE,the script will run as a loop
                         if (len(password)<10 and len(password)>20): #Password should be greater than 10 characters but less than 20
                            print("Password should be greater than 10 but less than 20 characters in length")
                            break
                         elif not re.search("[A-Z]",password): #Password should have a Uppercase letter or invalid
                            print("Uppercase Letter Required")
                            break
                         elif not re.search("[a-z]",password): #Password should have a lowercase letter or invalid
                            print("Lowercase letter required")
                            break
                         elif not re.search("[0-9]",password): #Password should have atleast one numerical value or invalid
                            print("One numerical value required in password")
                            break
                         elif not re.search("[!$#@%&*]",password): #A special character is required or invalid
                            print("A special character is required")
                            break
                         elif re.search("\s",password): #Invaild if a blank space is present
                            print("No blank spaces are allowed in your password")
                            break
                         else:
                            print("Password is Acceptable")
                            Y=False #When a valid password is created, the random variable Y is set to False and the loop is closed
                            break
                    if Y: #note this is outside the while loop (so the code jumps to it, if BREAK is typed inside the loop
                         print("Password is Invalid, Please try again")
                         main()

          main()
