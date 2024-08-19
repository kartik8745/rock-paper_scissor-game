# rock-paper_scissor-game
import random

def game():
    wins = {"player_scr": 0, "com_scr": 0}
    while True:
        choices = ["rock", "paper", "scissors"]
        player = input("Enter your choice (rock/paper/scissors) : ").lower()
        com_choice = random.choice(choices)
        
        print(f"\nPlayer choose {player}, computer choose {com_choice}.\n")

        if player == com_choice:
            print(f"Both players selected {player}. It's a tie!")
        elif player == "rock":
            if com_choice == "scissors":
                print("Rock smashes scissors! You win!")
                wins["player_scr"] += 1
            else:
                print("Paper covers rock! You lose.")
                wins["com_scr"] += 1
                
        elif player == "paper":
            if com_choice == "rock":
                print("Paper covers rock! You win!")
                wins["player_scr"] += 1
            else:
                print("Scissors cuts paper! You lose.")
                wins["com_scr"] += 1
                
        elif player == "scissors":
            if com_choice == "paper":
                print("Scissors cuts paper! You win!")
                wins["player_scr"] += 1
            else:
                print("Rock smashes scissors! You lose.")
                wins["com_scr"] += 1
                
        k=input("  wont to play again or not -> y or n :")
        if k=="n":
            break
    
    print(f"\nFinal score - Player_scr: {wins['player']}, Com_scr: {wins['com_scr']}")
    if wins["player_scr"]> wins["com_scr"]:
            print(" player won the  game !! ")
    else :
            print(" computer won the  game !! ")
   
game()
