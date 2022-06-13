# ZURI

def play ():
    user = input("what's your choice? 'r for rock, 'p for paper, 's for scissors\n")
    user = user.upper()

    computer = random.choice(['R', 'P', 'S'])
    
    if user == computer:
        return "you and the computer have both chosen {}. it's a tie.". format(computer)


    if is_win(user, computer):
        return "you have chosen{} and the computer has chosen{}. winner". format(user, computer)

    return "You have chosen {} and the computer has chosen. You lost". format(user, computer)

def is_win(player, opponent):
    # return true if the player beats the opponent
    # winning conditions R > S, S > P, P > R
    if (player == 'R' and opponent == 'S' and opponent == 'P') or (player == 'P' and opponent == 'S'):
        return True
    return False

if __name__ == '__main__':
    print(play())
