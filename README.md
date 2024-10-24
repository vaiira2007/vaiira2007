import turtle
import random

def petal():
    turtle.circle(20, 60)
    turtle.left(120)
    turtle.circle(20, 60)
    turtle.left(120)

def flower():
    # Pilih warna acak
    colors = ["pink", "yellow", "purple", "red", "blue"]
    turtle.color(random.choice(colors))
    turtle.begin_fill()
    for _ in range(6):
        petal()
        turtle.left(60)
    turtle.end_fill()

turtle.bgcolor("lightblue")
turtle.speed(5)

for x in range(-200, 200, 60):
    for y in range(-200, 200, 60):
        turtle.penup()
        turtle.goto(x, y)
        turtle.pendown()
        flower()

turtle.hideturtle()
turtle.done()
