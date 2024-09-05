# Dice_-simulator_project
import random

# Dice art dictionary
dice_art = {
    1: ("┌────────┐",
        "│        │",
        "|   ●    |",
        "|        |",
        "└────────┘"),

    2: ("┌────────┐",
        "│  ●     │",
        "|        |",
        "|      ● |",
        "└────────┘"),

    3: ("┌────────┐",
        "│  ●     │",
        "|    ●   |",
        "|      ● |",
        "└────────┘"),

    4: ("┌────────┐",
        "│  ●   ● │",
        "|        |",
        "|  ●   ● |",
        "└────────┘"),

    5: ("┌────────┐",
        "│  ●   ● │",
        "|    ●   |",
        "|  ●   ● |",
        "└────────┘"),

    6: ("┌────────┐",
        "│  ●   ● │",
        "|  ●   ● |",
        "|  ●   ● |",
        "└────────┘")
}

dice = []
total = 0
num_of_dice = int(input("How many dice?: "))

# Generate dice rolls
for _ in range(num_of_dice):
    dice.append(random.randint(1, 6))

# Display each die's art
for die in dice:
    for line in dice_art[die]:
        print(line)
    print()  # Adds a blank line between dice

# Calculate and display total
total = sum(dice)
print(f"Total: {total}")
