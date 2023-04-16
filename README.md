# Game
rock paper scissor game using python 

import random

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''



game_images = [rock,paper,scissors]
user_input = int(input("What do you choose? Type 0 for rock 1 for paper and 2 for scissors\n "))

if user_input >=3 or user_input < 0:
    print("You typed an invalid number, You lose")
else:
    print(game_images[user_input])

cpu = random.randint(0,2)
print("computer chose")
print(game_images[cpu])



if user_input ==0 and cpu == 2:
    print("You win!!")
elif cpu == 0 and user_input ==2:
    print("cpu wins!!")
elif cpu > user_input:
    print("Cpu wins!!")
elif user_input > cpu:
    print("You win!!")
elif cpu == user_input:
    print("Its a draw!!")
