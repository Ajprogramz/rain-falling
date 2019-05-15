import time
import random
import pygame
pygame.init()
pygame.mixer.music.load('rain-01.mp3')
pygame.mixer.music.play()
from turtle import*
wn = Screen()
wn.title('Purple rain by @krizzi studios')
wn.bgcolor('black')
txt = Turtle()
wn.register_shape('present.gif')
txt.shape('present.gif')
setup(width = 1000,height = 600)
time.sleep(7)
txt.hideturtle()
wn.bgpic('prg.gif')
setup(width = 800,height = 600)
colors = ['cyan','lime','deep pink','gold','silver','azure']
ps = []

for i in range(80):
 p = Turtle()
 p.speed(0)
 p.shape('square')
 p.shapesize(stretch_wid = 1, stretch_len = 0.1)
 p.color('white')
 p.up()
 p.goto(0,250)
 p.speed = random.randint(6,10)
 ps.append(p)
while True:
 wn.update()
 for p in ps:
    
    y = p.ycor()
    y-= p.speed + 100
    p.sety(y)
   
    if y < -200:
        x = random.randint(-380,380)
        y = random.randint(300,400)
        p.goto(x,y)
