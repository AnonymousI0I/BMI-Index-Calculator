# BMI Calculator

This Python script calculates the Body Mass Index (BMI) based on a user's weight in pounds and height in inches. The script categorizes the BMI result into underweight, normal, overweight, or obese.

## Features

- **Calculate BMI**: Users can input their weight and height to calculate their BMI.
- **Classify BMI**: Based on the calculated BMI, the script classifies the user as underweight, normal, overweight, or obese.
- **Input Validation**: The program validates user inputs to ensure proper functionality.

## Requirements

- Python 3.x

## Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/AnonymousI0I/BMI-Index-Calculator.git
    cd BMI-Index-Calculator
    ```

## Usage

1. **Run the script**:

    ```bash
    python BMI Calculate Program.py
    ```

2. **Follow the on-screen prompts to input your height and weight**.

### Example Usage

- You will be prompted to enter your height in inches and your weight in pounds.
- The script will calculate your BMI and classify it into one of the categories.

    Example:

    ```
    What is your height in inches?: 68
    What is your weight in pounds?: 150
    You are normal.
    ```

## Code Overview

### Function Descriptions

#### `calculate_bmi(weight_in_pounds, height_in_inches)`

Calculates the BMI based on weight in pounds and height in inches.

- **Parameters**:
  - `weight_in_pounds` (float): The weight in pounds.
  - `height_in_inches` (float): The height in inches.
- **Returns**:
  - `float`: The calculated BMI rounded to 1 decimal place.

## Contribution

Contributions are welcome! Please fork the repository, create a new branch, and submit a pull request.

### Main Function

The `main()` function orchestrates the workflow by prompting the user for inputs, calling the respective functions to perform BMI calculation, and displaying the results.

```python
def calculate_bmi(weight_in_pounds, height_in_inches):
    bmi = ((weight_in_pounds) / (height_in_inches * height_in_inches)) * 703
    return round(bmi, 1)

def main():
    height_in_inches = float(input("What is your height in inches?:"))
    weight_in_pounds = float(input("What is your weight in pounds?:"))
    
    bmi = calculate_bmi(weight_in_pounds, height_in_inches)

    if bmi <= 18.5:
        print("You are underweight.")
    elif 18.5 < bmi <= 24.9:
        print("You are normal.")
    elif 25 <= bmi <= 29.9:
        print("You are overweight.")
    else:
        print("You are obese.")

if __name__ == "__main__":
    main()

