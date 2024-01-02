import random

def get_user_choice():
    print("じゃんけんの手を選んでください")
    print("1. グー")
    print("2. チョキ")
    print("3. パー")
    choice = int(input("選択 (1-3): "))
    return choice

def get_computer_choice():
    return random.randint(1, 3)

def determine_winner(user_choice, computer_choice):
    print(f"あなたの選択: {user_choice}")
    print(f"コンピュータの選択: {computer_choice}")

    if user_choice == computer_choice:
        print("引き分けです。")
    elif (user_choice == 1 and computer_choice == 2) or \
         (user_choice == 2 and computer_choice == 3) or \
         (user_choice == 3 and computer_choice == 1):
        print("あなたの勝ちです！")
    else:
        print("コンピュータの勝ちです。")

def main():
    user_choice = get_user_choice()
    computer_choice = get_computer_choice()
    determine_winner(user_choice, computer_choice)

if __name__ == "__main__":
    main()
