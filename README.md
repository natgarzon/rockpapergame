#rockpapergame
#rock, paper, scissors basic

# varibles
CompChoice = 0
PlayerChoice = 0
import random


# functions
def ShowInstructions():
    print("You will be playing Rock, Paper or Scissors with a Computer.")
    
def GetPlayerChoice():
    strInput = input("Select Rock, Paper, or Scissors ").upper()
    PlayerChoice = strInput.upper()
    print("You choose: ",strInput)
    return strInput
    
def GetCompChoice():
    rndNum = random.randrange(1,4)
    if rndNum == 1:
        CompChoice = "ROCK"
        
    elif rndNum == 2:
        CompChoice = "PAPER"
    
    elif rndNum == 3:
        CompChoice = "SCISSORS"
    print("The Computer chooses: ",CompChoice)
    return CompChoice


def DeclareWinner(_PlayerChoice, _CompChoice):

    if _PlayerChoice == "ROCK" and _CompChoice == "SCISSORS":
        print("You WIN!")
    
    elif _PlayerChoice == "PAPER" and _CompChoice == "ROCK":
        print("You WIN!")
    
    elif _PlayerChoice == "SCISSORS" and _CompChoice == "PAPER":
        print("You WIN!")
        
    elif _PlayerChoice == _CompChoice:
        print("There is a TIE.")
    
    else:
        print("You LOSE!")
    


DeclareWinner(GetPlayerChoice(),GetCompChoice())
