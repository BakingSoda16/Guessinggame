# Guessing Game (Guess the number)
Python script with added sound effect when you guess correct number between 1-10

import random
from playsound import playsound

def guess(x):
    random_number = random.randint(1, x)
    guess = 0
    while guess != random_number:
        guess = int(input(f"Guess a random number between 1 and {x}: "))
#guess += 1, for each guess
        if guess < random_number:
            print ("Too low")
        elif guess > random_number:
            print ("Too high")

guess(10)
print ("You win")
playsound('Yay.wav')
