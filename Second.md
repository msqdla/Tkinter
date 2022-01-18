#### For Example[ ](https://github.com/msqdla/Tkinter/blob/main/Calculator%20App.md)004 Plus: 

```Python
from tkinter import *

root = Tk()
root.title("LAODA Calculator")

EntrySceen = Entry(root,bd=1,width=20)
EntrySceen.grid(padx=10,ipady=10)

def BPlus(number):
  EntrySceen.insert(0,number)

def BAddFuction():
  FirstNumber = EntrySceen.get()
  global f_num
  f_num = int(FirstNumber)
  EntrySceen.delete(0,END)

def BEqual():
  SecondNumber = EntrySceen.get()
  EntrySceen.delete(0,END)
  EntrySceen.insert(0,f_num + int(SecondNumber))


def BClear():
  EntrySceen.delete(0,END)

# Define Buttons
B1 = Button(root, text="1",command=lambda: BPlus(1))
B2 = Button(root, text="2",command=lambda: BPlus(2))
B3 = Button(root, text="3",command=lambda: BPlus(3))
BAdd = Button(root, text="+",command=BAddFuction)
BClearScreen = Button(root, text="Clear",command=BClear)
BEqualScreen = Button(root, text="=",command=BEqual)

# Put The Buttons On Screen
B1.grid(row=1,column=1)
B2.grid(row=1,column=2)
B3.grid(row=1,column=3)
BAdd.grid(row=3,column=1)
BClearScreen.grid(row=3,column=2)
BEqualScreen.grid(row=3,column=3)


root.mainloop()
```

## 第7章 用户输入和while循(2)

### 7.1 函数input()的工作原理

在本例中，Python运行第一行代码时，用户将看到提示Tell me something, and I will repeatit back to you:。程序等待用户输入，并在用户按回车键后继续运行。输入被赋给变量message，接下来的print(message)将输入呈现给用户……

```Python
message = input("Tell me something, and I will repeat it back to you: ")
print(message)
```

---

```Python
prompt = "If you tell us who you are, we can personalize the messages you see."
prompt += "\nWhat is your first name? "
name = input(prompt)
print(f"\nHello, {name}!")
```



### 7.1.2 使用int()来获取数值输入(3)

```Python
height = input("How tall are you, in inches? ")
height = int(height)

if height >= 48:    
  print("\nYou're tall enough to ride!")
else:    
  print("\nYou'll be able to ride when you're a little older.")

```

