import random

friend_count = int(input("Enter the number of friends joining (including you):\n"))
friend_lst = []

if friend_count <= 0:
    print("\nNo one is joining for the party")
    exit()
else:
    print("\nEnter the name of every friend (including you), each on a new line:")
    for count in range(friend_count):
        friend_lst.append(input())

    print("\nEnter the total bill value:")
    money = int(input())
    bill = round((money / friend_count), 2)
    friends_dict = dict.fromkeys(friend_lst, bill)

    print('\nDo you want to use the "Who is lucky?" feature? Write Yes/No:')
    lucky = input()
    if lucky == "No":
        print(friends_dict)
    else:
        lucky_name = random.choice(list(friends_dict.keys()))
        new_bill = int(round(money / (friend_count - 1), 2))
        friends_dict = dict.fromkeys(friend_lst, new_bill)
        friends_dict[lucky_name] = 0
        print(f"\n{friends_dict}")
