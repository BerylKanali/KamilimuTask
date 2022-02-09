## What is Git
Git is a version control system software that lets you manage and keep track of your source code history.

## What is Github
GitHub is a cloud-based hosting service that lets you manage Git repositories.

### Using loops to make your first game in Python
In this tutorial, I will show you how to use loops to create your first Rock,Scissors and Paper game.

---
**NOTE**
In Rock, Scissors and Paper: **Rock** smashes scissors.
                             **Paper** covers rock.
                             **Scissors** cut paper.
                             
---
#### 1.What is a loop
A sequence of instructions that is continually repeated until a certain condition is reached. We have **for** loops, **while** loops and **do** loops.

#### 2. Let us go through our code
We use import random to import the module that will randomize the computers choises in the game
```Python
import random
```
**User and Computer input**
We now ask the user to input his/her action
```Python
user_action = input("Enter a choice (rock, paper, scissors): ")
```
The computer will now randomly choose an action out of the options(possible actions) given
```Python
possible_actions = ["rock", "paper", "scissors"]
    computer_action = random.choice(possible_actions)
    print(f"\nYou chose {user_action}, computer chose {computer_action}.\n")
```    
**Create a loop of possible outcomes**
We now use a  if … elif … else block to compare the user and computer inputs and determine the winner.
Comparing the tie condition first is helpful so that we get rid of the need to compare each user action to each computer action that would make our code longer and cumbersome.

```Python
if user_action == computer_action:
        print(f"Both players selected {user_action}. It's a tie!")
    elif user_action == "rock":
        if computer_action == "scissors":
            print("Rock smashes scissors! You win!")
        else:
            print("Paper covers rock! You lose.")
    elif user_action == "paper":
        if computer_action == "rock":
            print("Paper covers rock! You win!")
        else:
            print("Scissors cuts paper! You lose.")
    elif user_action == "scissors":
        if computer_action == "paper":
            print("Scissors cuts paper! You win!")
        else:
            print("Rock smashes scissors! You lose.")
```
**Continue playing after the first try**
If a user would wish to play several rounds, we can add something to make it possible.
```Python
play_again = input("Play again? (y/n): ")
    if play_again.lower() != "y":
        break
```
We have to ask th player if they want to play again and ```break``` if they select no. without beaking the user will be asked to play again over and over until they terminate the console themselves.

---
**NOTE**
Variables are case sensitive so one has to be careful eith uppercase and lowecase letters when typing.

---
We have now created our first Rock, Paper and Scissors game!
