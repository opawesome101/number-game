https://roadmap.sh/projects/number-guessing-game



print("Welcome to number guesser 1.0!")
print("Rules: I will think of a number from 1-100. You must try and guess this number.")
print("If you guess wrong, I will tell you if the awnser is higher or lower than your guess.")
import random
awnser = random.randint(1,100)
guess = 0
while guess == False:
    diff = str(input("Select difficulty Easy Medium Hard ")).lower()
    if diff == "easy":
        guess = 10
    elif diff == "medium":
        guess = 5
    elif diff == "hard":
        guess = 3
print(f"{diff} mode: you have {guess} guesses")
original_guess = guess
user_awnser = int(input("Guess a number between 1-100 "))

while user_awnser != awnser:
    if user_awnser > awnser:
        print("Too high")
        guess = guess - 1
        print(f"Remaning guess {guess}")
        if guess == 0:
            print("You Lose!")
            replay = input("Try again? ")
        user_awnser = int(input("Guess a number between 1-100 "))
    elif user_awnser < awnser:
        print("Too low")
        guess = guess - 1
        print(f"Remaning guess {guess}")
        if guess == 0:
            print("You Lose!")
            replay = input("Try again? ")
        user_awnser = int(input("Guess a number between 1-100 "))

