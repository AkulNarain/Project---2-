#Project - 2


import random

# Generate a random number between 1 and 100
number = random.randint(1, 100)
attempts = 0

print("Welcome to the Number Guessing Game!")
print("I have picked a number between 1 and 100. Can you guess it?")

while True:
  try:
    guess_number = int(input("Enter your guess: "))
    attempts += 1 # Increment attempts with each valid guess
    
    if guess_number == number:
      print(f"Correct guess! You won the prize in {attempts} attempts.")
      break
    elif guess_number < number:
      print("Too low, try again.")
    else: # guess_number > number
      print("Too high, try again.")
  except ValueError:
    print("Invalid input. Please enter an integer.")
