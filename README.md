import turtle

# Setup screen
screen = turtle.Screen()
screen.bgcolor("black")
screen.title("Rotating Spiral Illusion")

t = turtle.Turtle()
t.speed(6)
t.width(2)
t.hideturtle()

# Smooth animation
screen.tracer(0)

angle_offset = 10

while True:
    t.clear()
    t.penup()
    t.goto(0, 0)
    t.pendown()

    length = 5   # SAME as first code (original size)

    for i in range(200):   # SAME density as first code
        if i % 2 == 0:
            t.pencolor("white")
        else:
            t.pencolor("black")

        t.forward(length)
        t.right(91 + angle_offset)
        length += 2   # SAME growth as original

    angle_offset += 0.1   # rotation speed

    screen.update()

# illution-graphic-
