## Roulette program

```py
from tkinter import *
import random
root = Tk()
root.geometry("400x500")

global thenumber
thenumber = random.randint(1,8)
global point; point = 0

def dsomething():
    global thenumber
    global goal; goal = 100
    global point
    global a;a = random.randint(1,8)
    if a == thenumber:
        root.destroy()
        ok = Tk()
        ok.geometry("200x300")
        Deathlabel = Label(ok, text=f"you died with {point} points").pack()
    point += a
    ScoreDisplay.config(text=str(point))

def rerollnum():
    global thenumber
    thenumber = random.randint(1,8)

Roulettebutton = Button(root, text="Roll roulette", command=dsomething, bg='red', fg="dark red")
Damn = Button(root, text="reroll", command=rerollnum)
ScoreDisplay = Label(root, text="0")
Roulettebutton.pack()#place(y=15,x=150)
ScoreDisplay.pack()
Damn.pack()

```