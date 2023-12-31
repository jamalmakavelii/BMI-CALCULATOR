# BMI-CALCULATOR
Python Code for BMI Calculator

def calculate_bmi(weight_kg, height_m):
    """
    Calculate BMI (Body Mass Index) using weight in kilograms and height in meters.
    
    :param weight_kg: Weight in kilograms (e.g., 70)
    :param height_m: Height in meters (e.g., 1.75)
    :return: BMI value
    """
    bmi = weight_kg / (height_m ** 2)
    return bmi

def interpret_bmi(bmi):
    """
    Interpret the BMI value and provide a category.

    :param bmi: BMI value
    :return: BMI category
    """
    if bmi < 18.5:
        return "Underweight"
    elif 18.5 <= bmi < 24.9:
        return "Normal weight"
    elif 25 <= bmi < 29.9:
        return "Overweight"
    else:
        return "Obese"

# Input from the user
weight = float(input("Enter your weight in kilograms: "))
height = float(input("Enter your height in meters: "))

# Calculate BMI
bmi = calculate_bmi(weight, height)

# Interpret and display the result
bmi_category = interpret_bmi(bmi)
print(f"Your BMI is {bmi:.2f}, which is considered '{bmi_category}'.")
