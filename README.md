# Guessinggame
Python script with added sound effect when you guess correct number between 1-10

import random
from playsound import playsound
# function for randomly generated number, you can either do this or something else.
# build a guessing game where the computer generates a number and you have to guess it.

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
