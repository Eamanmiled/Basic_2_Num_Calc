import tkinter
from tkinter import messagebox


# Function to generate password
def gen_num(num1, num2, add, multiply, divide):
    amount_of_ticked_boxes = 0
    if add:
        output = num1 + num2
        amount_of_ticked_boxes += 1

    if multiply:
        output = num1 * num2
        amount_of_ticked_boxes += 1

    if divide:
        output = num1 / num2
        amount_of_ticked_boxes += 1

    if amount_of_ticked_boxes != 1:
        messagebox.showwarning("Input Error", "Please tick one box")
        return ""
    else:
        return output


def update_num():
    try:
        num1 = int(num1_entry.get())
        num2 = int(num2_entry.get())
        add = add_var.get()
        multiply = multiply_var.get()
        divide = divide_var.get()
        result = gen_num(num1, num2, add, multiply, divide)
        num_entry.delete(0, tkinter.END)  # removes previous + adds new
        num_entry.insert(0, result)
    except ValueError:
        messagebox.showwarning("Input Error", "Please enter a numeric value for both boxes")


root = tkinter.Tk()
root.title("Basic 2 number Calculator")

tkinter.Label(root, text="First Digit").grid(row=0, column=0)
num1_entry = tkinter.Entry(root)
num1_entry.grid(row=0, column=1)

tkinter.Label(root, text="Second Digit").grid(row=1, column=0)
num2_entry = tkinter.Entry(root)
num2_entry.grid(row=1, column=1)

add_var = tkinter.BooleanVar()
tkinter.Checkbutton(root, text="Add?", variable=add_var).grid(row=2, column=0, sticky="w")

multiply_var = tkinter.BooleanVar()
tkinter.Checkbutton(root, text="Multiply?", variable=multiply_var).grid(row=3, column=0, sticky="w")

divide_var = tkinter.BooleanVar()
tkinter.Checkbutton(root, text="Divide?", variable=divide_var).grid(row=4, column=0, sticky="w")

tkinter.Button(root, text="Calculate", command=update_num).grid(row=5, column=0, columnspan=2)

tkinter.Label(root, text="Result:").grid(row=6, column=0)
num_entry = tkinter.Entry(root)
num_entry.grid(row=6, column=1)

root.mainloop()
