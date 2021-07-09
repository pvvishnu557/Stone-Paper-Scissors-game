# Stone-Paper-Scissors-game
Python code for Stone Paper Scissors game
import random
def print_menu():
    
    print("players in the game\n"
          +"Stone \n"
          +"Paper\n"
          +"Scissors\n")

    print("Game Rules are Here ^v^")
          
    print("Stone + Paper = Paper Wins")
    
    print("Scissors+ Stone = Stone wins")
    
    print("Paper + Scissors = Scissors")

name=input("Enter Your Name:")
print(name,"welcome to the game")
print_menu()

choice=True
while(choice):

    print("hi",name,"Select Your Choice")

    print("1.Stone \n"
          +"2.Paper \n"
          +"3.Scissors\n")

    choice=int(input("Enter Your Choice:"))
    while choice<1 or choice>3:
        
        choice=int(input("enter a valid input:"))
    if choice==1:
        choice_name="Stone"
    elif choice==2:
        choice_name="Paper"
    else:
        choice_name="Scissor"
    

    print(name,"your choice is",choice_name)

    print("now the computer turn!!!")

    computer_choice=random.randint(1,3)

    while computer_choice==choice:
        computer_choice=random.randint(1,3)
    if computer_choice==1:
        computer_choice_name="Stone"
    elif computer_choice==2:
        computer_choice_name="Paper"
    else:
        computer_choice_name="Scissor"
    print("computer choice is:",computer_choice_name)

    #matching between choice and cumputer choice

    if ((choice==1 and computer_choice==2)or(choice==2 and computer_choice==1)):

        print("paper wons ", end="")
        result="Paper"

    elif ((choice==2 and computer_choice==3) or(choice==3 and computer_choice==2)):

        print("Scissors wons ", end="")
        result="Scissors"

    else:

        print("Stone wons ", end="")
        result="Stone"


    if result==choice_name:
        print(name, " wons!!!\n"
              +"congratulations!!!")

    else:
        print(" computer wons!!!\n"
              +"better luck next time!!!")
        
    print("do you want to play?\n"
          +"YES= Y or y\n"
          +"NO= N Or n")

    ans=input()
    if ans== "n":
        choice=False
    
    
        print("Thank you",name)
        
