<h1 align="center"> Hirst Painting Project </h1>


<div align="center">
<img src="https://github.com/philoooo/Hirst-Painting-Project/blob/main/Screenshot%202025-10-30%20at%206.20.47%20PM.png" width="400" >
</div>


<h1></h1>

This project was inspired by Damien Hirst, a British artist known for his colorful dot paintings. I wanted to make my own version using Python. First, I used the colorgram module to extract colors from one of Hirst’s artworks. Then I used the turtle library to draw rows of dots on the screen. Each dot is randomly chosen from the color list, so the painting looks bright and different every time I run the program.

```
import colorgram

#extract colors from image
#colors = colorgram.extract('image.jpg', 30)

# rgb_colors = []
# colors = colorgram.extract('image.jpg', 30)
# for color in colors:
#     r = color.rgb.r
#     g = color.rgb.g
#     b = color.rgb.b
#     new_color = (r, g, b)
#     rgb_colors.append(new_color)
#
# print(rgb_colors)
import turtle
import random
from PIL.ImageChops import screen
turtle.colormode(255)
color_list = [(231, 206, 85), (218, 229, 219), (231, 222, 226), (224, 150, 89), (215, 224, 230), (120, 166, 185), (159, 14, 21), (34, 110, 157), (232, 82, 46), (124, 176, 144), (8, 97, 38), (171, 21, 16), (199, 65, 28), (185, 186, 27), (31, 128, 47), (12, 41, 74), (15, 63, 40), (242, 202, 5), (138, 82, 95), (85, 15, 22), (51, 166, 77), (44, 26, 22), (6, 65, 137), (173, 135, 149), (232, 170, 160), (48, 150, 195), (219, 66, 71), (74, 135, 186), (169, 206, 175)]

# create object
dot = turtle.Turtle()
dot.penup()
dot.hideturtle()
dot.setheading(225)
dot.forward(250)
dot.setheading(0)
dot.speed(10)
number_of_dots = 110


for dot_count in range(1, number_of_dots + 1):
    dot.dot(20, random.choice(color_list))
    dot.forward(50)

    if dot_count % 10 == 0:
        dot.setheading(90)
        dot.forward(50)
        dot.setheading(180)
        dot.forward(500)
        dot.setheading(0)


turtle.screensize()
turtle.exitonclick()

```
