- [https://tkdocs.com/tutorial/index.html](https://tkdocs.com/tutorial/index.html)
- [https://docs.python.org/3/library/tkinter.html#important-tk-concepts](https://docs.python.org/3/library/tkinter.html#important-tk-concepts)
- [https://tkdocs.com/shipman/button.html](https://tkdocs.com/shipman/button.html)

Some Webs
**（先是几个学的网，不会时能去查一下。）**

是从 Youtube
Python GUI's With TKinter
Codemy.com
一点点学起来。

边学边想——
#### Creating Buttons With TKinter - Python Tkinter GUI Tutorial

这一讲里说了 Button 的事。

|`state`|Set this option to `tk.DISABLED` to gray out the button and make it unresponsive. Has the value `tk.ACTIVE` when the mouse is over it. Default is `tk.NORMAL`.|
|-|-|
|`pady`|Additional padding above and below the text.|
|**`command`**|**Function or method to be called when the button is clicked.**|
|`activebackground`|Background [color](https://tkdocs.com/shipman/colors.html) when the button is under the cursor.|
|`activeforeground`|Foreground [color](https://tkdocs.com/shipman/colors.html) when the button is under the cursor.|

当你不会那个时你去看那个怎么讲，表里大多有。
一点点加，开头没用的先别放上来。

#### For Example Button 001:

这是头一：
先是 Install：
```pip ```

```Python
from tkinter import *

root = Tk()

def mc():
  ml = Label(root,text="121212",compound=LEFT,font=('Times', -60, 'bold')) #('Times', '24', 'bold italic')('Helvetica', '16') 
  ml.pack()

mB = Button(root,activeforeground="yellow",text="CM",bd="10",fg="red",highlightcolor="red",command=mc)
mB.pack()

root.mainloop()
```


