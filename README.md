# COS202-JIMOH-S-ASSIGNMENT-
This repository contains my python programming assignment (A mathematical calculator code and a pocket CGPA) and this code demonstrates the using  of fundamental programming concepts like variables ,conditional statements


QUESTIONS
1) Using PHYTON programming language, develop an interactive and well-designed screen 
MATHEMATICAL CALCULATOR (MC) programme containing components such as +, -, /, \, 
*, ^, %, C (Clear), OFF etc. (NB: It’s a simple calculator not complex scientific one).

2) CGPA is not something that should constrain you to visiting AVERS at all time – this is 
something you canl have inside your pocket and carry all around, running and checking it 
at your will. Using the powerful provision of selection control statements in PYTHON, 
develop a PERSONAL POCKET CGPA Calculator (PPC).

SOLUTION 1

print("")
print("   MATHEMATICAL CALCULATOR")
print("")
while True:
    print("\nMenu")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Modulus (%)")
    print("6. Power (^)")
    print("7. Square Root")
    print("8. Clear")
    print("9. OFF")
    choice = input("Choose an option: ")
    if choice == "9":
        print("Calculator Closed.")
        break
    elif choice == "8":
        print("\nScreen Cleared.")
        continue
    elif choice == "7":
        num = float(input("Enter number: "))
        print("Square Root =", num ** 0.5)
    elif choice in ["1","2","3","4","5","6"]:
        a = float(input("Enter first number: "))
        b = float(input("Enter second number: "))
        if choice == "1":
            print("Answer =", a + b)

        elif choice == "2":
            print("Answer =", a - b)
        elif choice == "3":
            print("Answer =", a * b)

        elif choice == "4":
            if b != 0:
                print("Answer =", a / b)
            else:
                print("Cannot divide by zero.")How was you day?
Ermmm 
Please I want to ask you something about the assignment
        elif choice == "5":
            print("Answer =", a % b)

        elif choice == "6":
            print("Answer =", a ** b)
    else:
        print("Invalid Choice.")


SOLUTION 2

print("")
print(" PERSONAL POCKET CGPA CALCULATOR")
print("")

courses = int(input("Enter number of courses: "))

total_points = 0
total_units = 0

for i in range(courses):
    print("\nCourse", i + 1)

    unit = int(input("Course Unit: "))
    score = int(input("Score: "))

    if score >= 70:
        grade = "A"
        point = 5

    elif score >= 60:
        grade = "B"
        point = 4

    elif score >= 50:
        grade = "C"
        point = 3

    elif score >= 45:
        grade = "D"
        point = 2

    elif score >= 40:
        grade = "E"
        point = 1

    else:
        grade = "F"
        point = 0

    quality = point * unit

    total_points += quality
    total_units += unit

    print("Grade:", grade)
    print("Grade Point:", point)

cgpa = total_points / total_units

print("")
print("Total Units =", total_units)
print("Total Quality Points =", total_points)
print("CGPA =", round(cgpa, 2))

if cgpa >= 4.50:
    print("Class: First Class")

elif cgpa >= 3.50:
    print("Class: Second Class Upper")

elif cgpa >= 2.40:
    print("Class: Second Class Lower")

elif cgpa >= 1.50:
    print("Class: Third Class")

else:
    print("Class: Pass")

