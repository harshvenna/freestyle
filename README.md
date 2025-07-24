import random

def guess_number():
    number = random.randint(1, 100)
    attempts = 0
    print("🎯 I'm thinking of a number between 1 and 100.")

    while True:
        try:
            guess = int(input("🔢 Take a guess: "))
            attempts += 1

            if guess < number:
                print("⬆️ Too low. Try again!")
            elif guess > number:
                print("⬇️ Too high. Try again!")
            else:
                print(f"✅ Correct! The number was {number}. You took {attempts} attempts.")
                break
        except ValueError:
            print("🚫 Please enter a valid number.")

if __name__ == "__main__":
    guess_number()
