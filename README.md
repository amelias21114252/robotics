# robotics
Unnamed repository; edit this file 'description' to name the repository.
from mblock import event
import time

@event.greenflag
def on_greenflag():
    sprite.say('Hi class!')
    sprite.pencolor('#f92bdd')
    sprite.pendown()
    for count in range(4):
        sprite.forward(100)
        sprite.right(90)
        time.sleep(1)

    sprite.penup()
    sprite.x = -46
    sprite.y = 110
    while True:
        sprite.set_costume('Bee1')
        time.sleep(1)
        sprite.set_costume('Bee2')
        time.sleep(1)
        sprite.play_until_done('')
