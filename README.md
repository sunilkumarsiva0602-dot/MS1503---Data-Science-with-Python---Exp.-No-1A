# Experiment 1.A  Employee Data Display Using Python

## Aim

To collect employee details, validate inputs, and calculate gross and net salary using Python.

## Algorithm

1. **Start** the program.
2. **Read Employee Details** from the user:
   * Input `name` (String) for the employee's full name.
   * Input `emp_id` (String) for the employee's identification number.
   * Input `basic` (Float) for the employee's basic salary.
3. **Validate Input**:
   * Ensure `basic` is a valid numeric value and check if `basic < 0`. If invalid or negative, display an appropriate error message and terminate the program.
4. **Compute Allowances**:
   * Calculate House Rent Allowance: $\text{HRA} = 0.15 \times \text{basic}$.
   * Calculate Dearness Allowance: $\text{DA} = 0.10 \times \text{basic}$.
5. **Compute Gross Salary**:
   * Calculate total earnings before deductions: $\text{Gross Salary} = \text{basic} + \text{HRA} + \text{DA}$.
6. **Compute Tax Deduction**:
   * Calculate income tax at $8\%$ of gross pay: $\text{Tax} = 0.08 \times \text{Gross Salary}$.
7. **Compute Net Salary**:
   * Calculate take-home pay: $\text{Net Salary} = \text{Gross Salary} - \text{Tax}$.
8. **Display Formatted Payroll Report**:
   * Print a structured summary displaying `name`, `emp_id`, `basic`, `HRA`, `DA`, `Gross Salary`, `Tax`, and `Net Salary` formatted to two decimal places.
9. **Stop** the program.

## Program
    def main():
        name = input("Enter Employee Name: ").strip()
        emp_id = input("Enter Employee ID: ").strip()

    if not name or not emp_id:
        print("Error: Employee Name and Employee ID cannot be empty.")
        return

    try:
        basic = float(input("Enter Basic Salary: "))
    except ValueError:
        print("Error: Basic salary must be a valid numeric value.")
        return

    if basic < 0:
        print("Error: Basic salary cannot be negative.")
        return

    hra = 0.15 * basic
    da = 0.10 * basic
    gross_salary = basic + hra + da
    tax = 0.08 * gross_salary
    net_salary = gross_salary - tax

    print("\n" + "=" * 42)
    print("           EMPLOYEE PAYROLL REPORT")
    print("=" * 42)
    print(f"Employee Name : {name}")
    print(f"Employee ID   : {emp_id}")
    print("-" * 42)
    print(f"Basic Salary  : {basic:10.2f}")
    print(f"HRA (15%)     : {hra:10.2f}")
    print(f"DA (10%)      : {da:10.2f}")
    print("-" * 42)
    print(f"Gross Salary  : {gross_salary:10.2f}")
    print(f"Tax (8%)      : {tax:10.2f}")
    print("-" * 42)
    print(f"Net Salary    : {net_salary:10.2f}")
    print("=" * 42)


if __name__ == "__main__":
    main()

## Output
  <img width="427" height="448" alt="image" src="https://github.com/user-attachments/assets/b4861e03-2294-4e63-9cb5-513014e86878" />
    

## ✅ Result

The program successfully accepts and validates employee details, calculates allowances and deductions, and displays a well-formatted salary report.
