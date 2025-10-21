# super-goggle圆形
import turtle
screen = turtle.Screen()
screen.setup(1200, 400)
screen.bgcolor("white")
t = turtle.Turtle()
t.speed(0)
t.color("red")
t.width(10)
t.penup()
start_x = -500
y_pos = 0
distances = [50, 60, 70, 80, 90, 100, 110, 120, 130]
for i in range(10):
    radius = 15 + i * 5
    if i == 0:
        t.goto(start_x, y_pos)
    else:
        t.goto(t.xcor() + distances[i-1], y_pos)
    t.pendown()
    t.circle(radius)
    t.penup()
t.hideturtle()
turtle.mainloop()
