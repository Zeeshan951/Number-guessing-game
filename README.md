# Number-guessing-game
Number guessing game using simple python 

import random as rd
guess_count=0
guess_limit=3
secret_number=rd.randint(1,10)
while guess_count<guess_limit:
    answer=int(input("Enter your number: "))
    if answer==secret_number:
        print("CORRECT!!")
        break
    elif answer>secret_number:
        print("Too high")
    elif answer<secret_number:
        print("Too low")
    else:
        print("wrong")
        guess_count=guess_count+1
if guess_count==guess_limit:
    print("Sorry..you ran out of chances.")
    print("The number was",secret_number)
