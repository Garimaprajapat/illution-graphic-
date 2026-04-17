ILLUSION GRAPHICS 
REPORT
Objective
The primary objective of this program is to design and display a rotating spiral illusion using Python’s turtle graphics module. The program demonstrates how incremental geometric transformations, combined with animation techniques, can produce a visually engaging and dynamic illusion. It also helps in understanding the concepts of loops, angles, and real-time rendering.
 

Tools and Technologies Used

• Python Programming Language: Used to implement the logic and control the flow of the program. • Turtle Graphics Module: A standard Python library that allows users to create drawings and animations by controlling a cursor (turtle) on the screen

Detailed Code Explanation
1.	Importing the Required Module import turtle The program begins by importing the turtle module, which provides the necessary functions to create graphical patterns and animations. This module acts as the foundation for all drawing operations in the program.

2.	Screen Initialization and Configuration screen = turtle.Screen() screen.bgcolor("black") screen.title("Rotating Spiral Illusion") A graphical window (screen) is initialized to display the output. The background color is set to black to enhance contrast and improve visibility of the drawing. Additionally, a title is assigned to the window to describe the purpose of the program.

3.	Turtle Object Creation and Setup t = turtle.Turtle() t.speed(6) t.width(2) t.hideturtle() A turtle object is created, which acts as a drawing pen. Its speed is set to a moderate level to balance performance and visual clarity. The width of the drawing line is adjusted to improve visibility, and the turtle cursor is hidden to ensure a clean and distraction-free animation.

4.	 Enabling Smooth Animation screen.tracer(0) The automatic screen updates are disabled using the tracer function. This allows the program to manually control when the screen refreshes, resulting in smoother and more efficient animation.

5.	 Initialization of Rotation Parameter angle_offset = 10 An initial angle offset is defined. This variable plays a crucial role in creating the illusion of rotation by slightly modifying the turning angle during each frame of the animation.

6.	 Continuous Animation Loop while True: An infinite loop is used to continuously redraw the pattern. Each iteration of the loop represents a new frame, thereby creating a seamless animation effect.

7.	Resetting the Drawing State t.clear() t.penup() t.goto(0, 0) t.pendown() At the beginning of each frame, the previous drawing is cleared. The turtle is repositioned to the center of the screen without drawing, and then drawing is resumed. This ensures that each frame starts from a consistent position.

8.	Initial Line Length Setup length = 5 A variable is initialized to define the starting length of each line segment. This value gradually increases during the drawing process, contributing to the spiral formation. Constructing the Spiral Pattern for i in range(200):A loop runs 200 times to construct the spiral. Each iteration represents one segment of the spiral. Color Alternation Mechanism if i % 2 == 0: t.pencolor("white") else: t.pencolor("black") The pen color alternates between white and black based on whether the loop index is even or odd. This contrast enhances the illusion and adds depth to the pattern. Movement and Rotation Logic t.forward(length) t.right(91 + angle_offset) length += 2 The turtle moves forward by a certain length and then rotates slightly more than 90 degrees. The addition of the angle offset ensures that the shape does not form a perfect square, but instead develops into a spiral. The length is incremented after each step, causing the spiral to expand outward progressively.

9.	Dynamic Rotation Adjustment angle_offset += 0.1 After each frame, the angle offset is slightly increased. This gradual change is responsible for producing the effect of rotation in the spiral pattern

10.	Manual Screen Update screen.update() The screen is manually updated at the end of each loop iteration. This displays the newly drawn frame and ensures smooth animation. Working Principle of the Illusion The rotating spiral illusion is achieved through a combination of mathematical and visual techniques: 

11.	• A slight deviation from a 90-degree angle creates a spiral instead of a square.

12.	 • The continuous increase in line length results in outward expansion.

13.	 • The incremental change in angle offset produces a rotational effect across frames. 

14.	• The alternating color scheme enhances contrast and strengthens the illusion. Program Flow Summary.

1. Initialize the screen and turtle settings.
 2. Enter an infinite loop for animation. 
3. Clear previous drawings and reset position. 
4. Draw a spiral using a loop with increasing length and angle.
 5. Slightly adjust the rotation angle.
 6. Update the screen to display the new frame.
 7. Repeat the process continuously.

Output Description
 The program generates a continuously evolving spiral pattern that appears to rotate smoothly. The animation is visually appealing and demonstrates how simple programming logic can create complex graphical effects.


Conclusion 
This program effectively illustrates how basic geometric transformations and incremental changes can produce sophisticated visual illusions. It highlights the power of Python’s turtle graphics in creating animations and serves as an excellent example for learning concepts such as loops, conditionals, and real-time rendering. The project is both educational and visually engaging, making it suitable for beginners exploring graphical programming.

By :
1.	Bhave sharma  (243501031)
2.	Garima prajapat  (243501054)
3.	Liya joseph (243501109)
4.	Khushboo upadhyay (243501089)

___________________________________________________________________________________________________________________________________________________________________

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


