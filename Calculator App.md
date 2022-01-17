还是从 Youtube Python GUI's With TKinter [Codemy.com](http://Codemy.com) 一点点学起来。

学的是——

#### Continue Building A Simple Calculator App - Python Tkinter GUI Tutorial #6

从能用的东西学起来，这次是他讲的计算器的第二讲，没太涉及Tkinter多讲的是Python里的一些函数，我大约就是按着他讲到那就学到那。这次讲到了`inser`、`return`、 global……

我整理了一下他写出来的代码如下：

#### For Example 004:

```Python
from tkinter import *

root = Tk()
root.title("LAODA Calculator")

EntrySceen = Entry(root,bd=1,width=20)
EntrySceen.grid(padx=10,ipady=10)

def BPlus(number):
  EntrySceen.insert(0,number)

def BAddFuction():
  fist_number = EntrySceen.get()
  global fist_num
  f_num = int(fist_number)

def BClear():
  EntrySceen.delete(0,END)

# Define Buttons
B1 = Button(root, text="1",command=lambda: BPlus(1))
B2 = Button(root, text="2",command=lambda: BPlus(2))
B3 = Button(root, text="3",command=lambda: BPlus(3))
BAdd = Button(root, text="+",command=BAddFuction)
BClearScreen = Button(root, text="Clear",command=BClear)

# Put The Buttons On Screen
B1.grid(row=1,column=1)
B2.grid(row=1,column=2)
B3.grid(row=1,column=3)
BAdd.grid(row=3,column=1)
BClearScreen.grid(row=3,column=2)


root.mainloop()
```

对于不懂的一些函数就从《Python编程：从入门到实践（第2版）》查一下看一看学一学。

#### 在列表中插入元素

使用方法**`insert()`**可在列表的任何位置添加新元素。为此，你需要指定新元素的索引和值。

  motorcycles = ['honda', 'yamaha', 'suzuki']

```Python
motorcycles.insert(0, 'ducati')
print(motorcycles)

```

在这个示例中，值'ducati'被插入到了列表开头（见❶）。方法insert()在索引0处添加空间，并将值'ducati'存储到这个地方。这种操作将列表中既有的每个元素都右移一个位置：

['ducati', 'honda', 'yamaha', 'suzuki']

#### 返回值

函数并非总是直接显示输出，它还可以处理一些数据，并返回一个或一组值。函数返回的值称为返回值。在函数中，可使用`return`语句将值返回到调用函数的代码行。返回值让你能够将程序的大部分繁重工作移到函数中去完成，从而简化主程序。
