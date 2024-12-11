# PYTHON-DICE-ROLLING-SIMULATOR.....
This repository contains a simplified Python Project dipicting the rolling of dice simulator, focusing on the random generation of numbers ranged within dices.

# SOURCE CODE.....
import random

# UNICODE CHARACTERS
# print("\u25CF \u250C \u2500 \u2510 \u2502 \u2514 \u2518")
# ● ┌ ─ ┐ │ └ ┘

# "┌─────────┐"
# "│         │"
# "│         │"
# "│         │"
# "└─────────┘"

# CREATING DICTIONARY
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
