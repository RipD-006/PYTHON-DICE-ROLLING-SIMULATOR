# PYTHON-DICE-ROLLING-SIMULATOR.....
This repository contains a simplified Python Project dipicting the rolling of dice simulator, focusing on the random generation of numbers ranged within dices.

# UNICODE CHARACTERS
The first step in creating a responsive Dice Roller, we import the random module to fetch any random value within the range (1 to 6)
With the help of Unicode characters we create a the necessary templates representing the faces of the dice. The Unicode Characters used are as follows: 

    print("\u25CF \u250C \u2500 \u2510 \u2502 \u2514 \u2518")
    ● ┌ ─ ┐ │ └ ┘

    "┌─────────┐"
    "│         │"
    "│         │"
    "│         │"
    "└─────────┘"

Hence, it is time to proceed with the third step in creating a Python Dictionary containing Tuples of (Key:Value) pairs which our program would take reference from in displaying the faces of the Dices.

# CREATING AN EMPTY LIST AND SETTING THE INIIAL VALUE OF SUM TOTAL OF NUMBERS DISPLAYED ON EACH DICE.
    dice =[]    
    total = 0   # INITIAL TOTAL FOR SUM OF ALL THE DICES

# USER'S INPUT
    number_of_dices = int(input("Enter the number of Dice: "))

# CREATING FOR LOOP
Here, the User entered value for the number of dices to be rolled is appended to the Empty List (i.e. dice=[]) such that the Random Module displays a number ranging from 1 to 6 on each dice that has been rolled.
    
    for die in range(number_of_dices):
        dice.append(random.randint(1, 6))


The significance of the second for loop is all about displaying the faces of each dice in an ordered way next to one another whenever the output is displayed.
    
    for item in range(5):
        for die in dice:
            print(dice_art.get(die)[item], end="")
        print()


The final for loop is responsible for the sum of all the values on the faces displayed when the dices were rolled. This iteration will run according to the value of the number of dices to be rolled which was previously specified by the user and the faces of each dice is added to the total variable replacing the previous value with the sum of all the outcomes.

    for die in dice:
        total += die
    print(f"Total : {total}")

The program terminates when the total for all the outcomes is displayed to the user as output.

# AUTHOR INFO
    Name     : Ripan Das
    GitHub   : RipD-006 [Url : https://github.com/RipD-006]
    LinkedIn : https://www.linkedin.com/in/ripan-das-375b33286
