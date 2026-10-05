# CodeOrbit Tech Internship
# Task 1: Simple Calculator

# Function to perform calculations
def calculate(num1, num2, operator):

    if operator == "+":
        return num1 + num2

    elif operator == "-":
        return num1 - num2

    elif operator == "*":
        return num1 * num2

    elif operator == "/":
        # Division by zero is not allowed
        if num2 == 0:
            raise ZeroDivisionError("Cannot divide by zero.")

        return num1 / num2

    else:
        raise ValueError("Invalid operator.")


# Display calculator title
print("=" * 40)
print("       SIMPLE CALCULATOR")
print("=" * 40)

try:
    # Get numbers from the user
    num1 = float(input("Enter the first number: "))
    num2 = float(input("Enter the second number: "))

    # Display available operations
    print("\nChoose an operation:")
    print("+  Addition")
    print("-  Subtraction")
    print("*  Multiplication")
    print("/  Division")

    # Get operator from the user
    operator = input("Enter operator (+, -, *, /): ")

    # Calculate result
    result = calculate(num1, num2, operator)

    # Display result
    print("\n" + "-" * 40)
    print(f"Result: {num1} {operator} {num2} = {result}")
    print("-" * 40)

except ValueError:
    print("\nError: Please enter valid numbers and a valid operator.")

except ZeroDivisionError as error:
    print(f"\nError: {error}")

except Exception as error:
    print(f"\nAn unexpected error occurred: {error}")
