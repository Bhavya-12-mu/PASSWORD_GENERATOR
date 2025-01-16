import random
import string

def generate_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for i in range(length))
    return password
try:
    length = int(input("Enter the desired password length: "))
    if length <= 0:
        print("Password length should be a positive number.")
    else:
        password = generate_password(length)
        print("Generated password:", password)
except ValueError:
    print("Please enter a valid number.")
