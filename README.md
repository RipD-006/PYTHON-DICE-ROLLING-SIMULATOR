# PYTHON-DICE-ROLLING-SIMULATOR.....
This repository contains a simplified Python Project dipicting the rolling of dice simulator, focusing on the random generation of numbers ranged within dices.

The first step in creating a responsive Dice Roller, we import the random module to fetch any random value within the range (1 to 6)
With the help of Unicode characters we create a the necessary templates representing the faces of the dice. The Unicode Characters used are as follows: 

# UNICODE CHARACTERS
print("\u25CF \u250C \u2500 \u2510 \u2502 \u2514 \u2518")
● ┌ ─ ┐ │ └ ┘

"┌─────────┐"
"│         │"
"│         │"
"│         │"
"└─────────┘"

Hence, it is time to proceed with the third step in creating a Python Dictionary containing Tuples of (Key:Value) pairs which our program would take reference from in displaying the faces of the Dices.


dice_art = {
    1:("┌─────────┐",
       "│         │",
       "│    ●    │",
       "│         │",
       "└─────────┘"),
    2:("┌─────────┐",
       "│  ●      │",
       "│         │",
       "│      ●  │",
       "└─────────┘"),
    3:("┌─────────┐",
       "│  ●      │",
       "│    ●    │",
       "│      ●  │",
       "└─────────┘"),
    4:("┌─────────┐",
       "│  ●   ●  │",
       "│         │",
       "│  ●   ●  │",
       "└─────────┘"),
    5:("┌─────────┐",
       "│  ●   ●  │",
       "│    ●    │",
       "│  ●   ●  │",
       "└─────────┘"),
    6:("┌─────────┐",
       "│  ●   ●  │",
       "│  ●   ●  │",
       "│  ●   ●  │",
       "└─────────┘")
}

dice =[]    # CREATING EMPTY LIST
total = 0   # INITIAL TOTAL FOR SUM OF ALL THE DICES 
number_of_dices = int(input("Enter the number of Dice: "))

# CREATING FOR LOOP
for die in range(number_of_dices):
    dice.append(random.randint(1, 6))

for item in range(5):
    for die in dice:
        print(dice_art.get(die)[item], end="")
    print()


for die in dice:
    total += die

print(f"Total : {total}")
