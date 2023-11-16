# milestone_3.py
Hangman Project_Milestone 3
# Create a while loop and set the condition to True.
while True:
    # Ask the user to guess a letter and assign this to a variable called guess.
    guess = input("Guess a letter: ")

    # Check that the guess is a single alphabetical character.
    if len(guess) == 1 and guess.isalpha():
        # If the guess passes the checks, break out of the loop.
        break
    else:
        # If the guess does not pass the checks, then print a message.
        print("Invalid letter. Please, enter a single alphabetical character.")
  import random

# Assume a list of possible words
word_list = ["apple", "banana", "orange", "strawberry", "blueberry"]

# Create an if statement that checks if the guess is in the word.
secret_word = random.choice(word_list)

# User input loop
while True:
    guess = input("Guess a letter: ")

    if len(guess) == 1 and guess.isalpha():
        # Check if the guess is in the word.
        if guess in secret_word:
            # Print a message saying "Good guess! {guess} is in the word."
            print(f"Good guess! {guess} is in the word.")
        else:
            # Print a message saying "Sorry, {guess} is not in the word. Try again."
            print(f"Sorry, {guess} is not in the word. Try again.")
        break  # Break out of the loop after processing the guess
    else:
        print("Invalid letter. Please, enter a single alphabetical character.")


import random

# Assume a list of possible words
word_list = ["apple", "banana", "orange", "strawberry", "blueberry"]

# Create an if statement that checks if the guess is in the word.
secret_word = random.choice(word_list)

# User input loop
while True:
    guess = input("Guess a letter: ")

    if len(guess) == 1 and guess.isalpha():
        # Step 1: Check if the guess is in the word.
        if guess in secret_word:
            # Step 2: Print a message saying "Good guess! {guess} is in the word."
            print(f"Good guess! {guess} is in the word.")
        else:
            # Step 3: Print a message saying "Sorry, {guess} is not in the word. Try again."
            print(f"Sorry, {guess} is not in the word. Try again.")
        break  # Break out of the loop after processing the guess
    else:
        # Step 3: Print a message saying "Sorry, {guess} is not in the word. Try again."
            print(f"Sorry, {guess} is not in the word. Try again.")
        break  # Break out of the loop after processing the guess
    else:
        print("Invalid letter. Please, enter a single alphabetical character.")
Invalid letter. Please, enter a single alphabetical character

import random

# Assume a list of possible words
word_list = ["apple", "banana", "orange", "strawberry", "blueberry"]

# Step 1: Define a function called check_guess.
def check_guess(guess):
    # Step 2: Convert the guess into lower case.
    guess = guess.lower()

    # Step 3: Check if the guess is in the word.
    if guess in secret_word:
        print(f"Good guess! {guess} is in the word.")
    else:
        print(f"Sorry, {guess} is not in the word. Try again.")

# Define a function called ask_for_input.
def ask_for_input():
    # User input loop
    while True:
        guess = input("Guess a letter: ")

        if len(guess) == 1 and guess.isalpha():
            # Step 3: Call the check_guess function to check if the guess is in the word.
            check_guess(guess)
            break  # Break out of the loop after processing the guess
        else:
            print("Invalid letter. Please, enter a single alphabetical character.")

# Choose a random word from the word list
secret_word = random.choice(word_list)

# Outside the function, call the ask_for_input function to test your code.
ask_for_input()



import random

class Hangman:
    def __init__(self, word_list, num_lives=5):
        # Step 3: Initialize attributes
        self.word_list = word_list
        self.num_lives = num_lives
        self.list_of_guesses = []
        self.word = self.choose_random_word()
        self.word_guessed = ['_'] * len(self.word)
        self.num_letters = len(set(self.word))

    def choose_random_word(self):
        # Helper method to choose a random word from the word list
        return random.choice(self.word_list)

