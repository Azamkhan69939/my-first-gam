# my-first-gam
# ROCK, PAPER, SCISSOR Game
#my first game

import random


def game(comp, you):
    if you == comp:
        return None
    elif comp == 'r':
        if you == 'p':
            return True
        elif you == 's':
            return False
    elif comp == 'p':
        if you == 's':
            return True
        elif you == 'r':
            return False
    elif comp == 's':
        if you == 'r':
            return True
        elif you == 'p':
            return False


start = (input(
    "Rock, paper and Scrissor game,\nEnter Start to Enter the game:\n"))
start = start.lower()
if start == "start":
    for games in range(10, -1, -1):
        numr = random.randint(1, 3)
        if numr == 1:
            computer = 'r'
        elif numr == 2:
            computer == 'p'
        elif numr == 3:
            computer == 's'
        you = input(
            "Enter r for Rock,  Enter s for Scissor,  Enter p for Paper:\n")
        a = game(computer, you)
        print(f"you choose: {you} and computer choose: {computer}")
        if a == None:
            print("the game has tied")
        elif a == True:
            print("you won")
            games == 10
        elif a == False:
            print("you lose")
        print(f"you have {games} life left")
else:
    print("Enter the correct value")
