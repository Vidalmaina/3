num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))
operation = input("Enter the operation (+, -, *, /): ").strip()

# Define the operations using a dictionary
operations = {
    '+': lambda a, b: a + b,
    '-': lambda a, b: a - b,
    '*': lambda a, b: a * b,
    '/': lambda a, b: None if b == 0 else a / b
}

# Perform the calculation and print the result
if operation in operations:
    result = operations[operation](num1, num2)
    if result is None:
        print("Error: Division by zero is not allowed.")
    else:
        print(f"{num1:g} {operation} {num2:g} = {result:g}")
else:
    print("Error: Invalid operation.")# 3
