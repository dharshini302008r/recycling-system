# recycling-system
# coding 
print("AI Based Recycling System")
print("------------------------")

waste = input("Enter waste type (plastic/paper/metal/glass): ").lower()

if waste == "plastic":
    print("Waste classified as Plastic")
    print("Move to Plastic Recycling Bin")

elif waste == "paper":
    print("Waste classified as Paper")
    print("Move to Paper Recycling Bin")

elif waste == "metal":
    print("Waste classified as Metal")
    print("Move to Metal Recycling Bin")

elif waste == "glass":
    print("Waste classified as Glass")
    print("Move to Glass Recycling Bin")

else:
    print("Unknown Waste Type")
    print("Manual Inspection Required")
from tkinter import *
from tkinter import filedialog
from PIL import Image

root = Tk()
root.title("AI Based Recycling System")
root.geometry("400x300")

def classify():
    file = filedialog.askopenfilename()

    if "plastic" in file.lower():
        result.config(text="Plastic Waste Detected")
    elif "paper" in file.lower():
        result.config(text="Paper Waste Detected")
    elif "metal" in file.lower():
        result.config(text="Metal Waste Detected")
    elif "glass" in file.lower():
        result.config(text="Glass Waste Detected")
    else:
        result.config(text="Unknown Waste")

Button(root, text="Upload Image", command=classify).pack(pady=20)

result = Label(root, text="")
result.pack()

root.mainloop()
# output

