import tkinter as tk 
import random

CANVAS_WIDTH = 300
CANVAS_HEIGHT = 400
CIRCLE_RADIUS = 20
def draw_circle():
 x = random.randint(CIRCLE_RADIUS,CANVAS_WIDTH-CIRCLE_RADIUS)
 y = random.randint(CIRCLE_RADIUS,CANVAS_WIDTH-CIRCLE_RADIUS)

 canvas.create_oval(
   x - CIRCLE_RADIUS, y - CIRCLE_RADIUS,
                     x + CIRCLE_RADIUS, y + CIRCLE_RADIUS,
                     fill="blue",outline="black"
                     )
root = tk.Tk()
root.title("Simple Circle Drawer")

canvas = tk.Canvas(root,width=CANVAS_WIDTH,height=CANVAS_HEIGHT,bg="white")
canvas.pack()

button = tk.Button(root,text="Draw Circle",command=draw_circle)
button.pack()

root.mainloop()
