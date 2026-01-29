# OYEE MANAGEMENT SYSTEM - Employee Management Project

employees = []

def add_employee():
    print("\n--- Add Employee ---")
    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID: ")
    email = input("Enter Employee Email: ")
    age = input("Enter Employee Age: ")
    position = input("Enter Position: ")
    shift = input("Enter Working Shift (e.g. 5 to 9): ")
    
    employee = {
        "name": name,
        "id": emp_id,
        "email": email,
        "age": age,
        "position": position,
        "shift": shift,
        "status": "Shift Active"
    }
    
    employees.append(employee)
    print("✅ Employee Added Successfully!\n")

def view_employees():
    print("\n--- Employee List ---")
    if len(employees) == 0:
        print("No employees found!")
    else:
        for emp in employees:
            print("----------------------------")
            print("Employee Name:", emp["name"])
            print("Employee ID:", emp["id"])
            print("Email:", emp["email"])
            print("Age:", emp["age"])
            print("Position:", emp["position"])
            print("Working Shift:", emp["shift"])
            print("Status:", emp["status"])
            print("----------------------------")

def shift_over():
    emp_id = input("Enter Employee ID to end shift: ")
    for emp in employees:
        if emp["id"] == emp_id:
            emp["status"] = "Shift Over | Period Ended"
            print("✅ Shift Ended Successfully!")
            return
    print("❌ Employee not found!")

def total_employees():
    print("\nTotal Employees:", len(employees))

def menu():
    while True:
        print("\n===== OYEE MANAGEMENT SYSTEM =====")
        print("1. Add Employee")
        print("2. View Employees")
        print("3. Shift Over")
        print("4. Total Employees")
        print("5. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            add_employee()
        elif choice == "2":
            view_employees()
        elif choice == "3":
            shift_over()
        elif choice == "4":
            total_employees()
        elif choice == "5":
            print("👋 Exiting System...")
            break
        else:
            print("❌ Invalid choice! Try again.")

menu()
