# calculator-in-python
A modular Python-based calculator capable of performing basic arithmetic and advanced mathematical operations with a clean, user-friendly interface.
print("Select operation:")
print("1. Add")
print("2. Subtract")
print("3. Multiply")
print("4. Divide")
print("5. LCM")
print("6. HCF")
print("7. factors")
choice = input("Enter choice (1/2/3/4/5/6/7): ")
if choice in ('1', '2', '3', '4'):
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))
    if choice == '1':
        print(num1, "+", num2, "=", num1 + num2)
    elif choice == '2':
        print(num1, "-", num2, "=", num1 - num2)
    elif choice == '3':
        print(num1, "*", num2, "=", num1 * num2)
    elif choice == '4':
        if num2 != 0:
            print(num1, "/", num2, "=", num1 / num2)
        else:
            print("Error: Division by zero is not allowed.")

elif choice == '5':
    def compute_lcm(x, y):
        if x > y:
            greater = x
        else:
            greater = y
        while(True):
            if((greater % x == 0) and (greater % y == 0)):
                lcm = greater
            break
        greater += 1
        return lcm
    num1 = int(input("Enter first number: "))
    num2 = int(input("Enter second number: "))
    print("The L.C.M. is", compute_lcm(num1, num2))

elif choice == '6':
    def compute_hcf(x, y):
        if x > y:
            smaller = y
        else:
            smaller = x
        for i in range(1, smaller + 1):
            if((x % i == 0) and (y % i == 0)):
                hcf = i
        return hcf
    num1 = int(input("Enter first number: "))
    num2 = int(input("Enter second number: "))
    print("The H.C.F. is", compute_hcf(num1, num2))

elif choice == '7':
    num = int(input("Enter a number: "))
    print("The factors of", num, "are:")
    for i in range(1, num + 1):
        if num % i == 0:
            print(i)
else:
    print("Invalid input. Please enter a valid operation.")

