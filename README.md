from tkinter import *

root = Tk()
root.title("Restaurant Bill System")
root.geometry("400x450")

item1 = IntVar()
item2 = IntVar()
item3 = IntVar()

def calculate_bill():
    price1 = item1.get() * 50   
    price2 = item2.get() * 30  
    price3 = item3.get() * 20 
    
    total = price1 + price2 + price3
    result_label.config(text=f"Total Bill: ₹{total}")

Label(root, text="🍽️ Restaurant Bill System", font=("Arial", 16, "bold")).pack(pady=10)

frame = Frame(root)
frame.pack(pady=10)

Label(frame, text="Burger (₹50): ").grid(row=0, column=0, padx=10, pady=5)
Entry(frame, textvariable=item1).grid(row=0, column=1)

Label(frame, text="Pizza (₹30): ").grid(row=1, column=0, padx=10, pady=5)
Entry(frame, textvariable=item2).grid(row=1, column=1)

Label(frame, text="Tea (₹20): ").grid(row=2, column=0, padx=10, pady=5)
Entry(frame, textvariable=item3).grid(row=2, column=1)

Button(root, text="Calculate Bill", command=calculate_bill, bg="green", fg="white").pack(pady=20)

result_label = Label(root, text="Total Bill: ₹0", font=("Arial", 14))
result_label.pack()

root.mainloop()
