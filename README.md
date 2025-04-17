# endsem
def calculate_salary(hourly_rate, hours_worked, tax_rate=0.15):
    """
    This function calculates the net salary of an employee based on their hourly rate,
    hours worked, and tax rate. The function first computes the gross salary by multiplying
    hourly rate by hours worked, then deducts the tax, and finally returns the net salary.
    
    Parameters:
    hourly_rate (float): The hourly wage of the employee.
    hours_worked (float): The number of hours worked by the employee.
    tax_rate (float): The tax rate to be applied on the gross salary (default is 0.15).
    
    Returns:
    float: The net salary after tax deduction.
    """
    # Compute gross salary
    gross_salary = hourly_rate * hours_worked
    
    # Deduct tax from the gross salary
    tax_deduction = gross_salary * tax_rate
    net_salary = gross_salary - tax_deduction
    
    return net_salary

def main():
    # Get user input for hourly rate and hours worked
    try:
        hourly_rate = float(input("Enter hourly rate: "))
        hours_worked = float(input("Enter hours worked: "))
        
        # Ensure that the input values are non-negative
        if hourly_rate < 0 or hours_worked < 0:
            print("Hourly rate and hours worked must be non-negative numbers.")
        else:
            # Call the function to calculate the net salary
            net_salary = calculate_salary(hourly_rate, hours_worked)
            
            # Print the net salary in a formatted manner
            print(f"Net Salary: {net_salary:,.2f}")
    
    except ValueError:
        print("Invalid input. Please enter valid numerical values for hourly rate and hours worked.")

# Call the main function to execute the program
if __name__ == "__main__":
    main()
