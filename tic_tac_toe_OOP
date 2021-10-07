# Tic Tac Toe OOP
# Tom S.
# 09/17/2021
# Shortly after creating my previous Tic Tac Toe game,
# I immediately created this one as I started to learn
# OOP and decided to rewrite Tic Tac Toe while implementing
# OOP characteristics to my game. I also added more features
# such as a scoreboard and the ability to continue playing.

import random
import sys

class tic_tac_toe:
    def __init__(self):
        self.game_active = True
        self.player_score = 0
        self.cpu_score = 0
        self.player_unit = str
        self.cpu_unit = str
        self.game_board = ['-','-','-','-','-','-','-','-','-']


    def game_setup(self):
        print('Welcome to Tic-Tac-Toe!')
        print('Press 1 to play as X. Press 2 to play as O.')
        self.x_or_o = input('')
        if self.x_or_o == '1':
            print('You are X. CPU will be O.')
            self.player_unit = 'X'
            self.cpu_unit = 'O'
            return
        elif self.x_or_o == '2':
            print('You are O. CPU will be X.')
            self.player_unit = 'O'
            self.cpu_unit = 'X'
            return
        else:
            print('That was not a valid choice. Try again.')
            tic_tac_toe.game_setup()
            return

    def game_score(self):
        self.player_score_border = [' ',' ',' ','|']
        self.cpu_score_border = [' ',' ',' ','*']

        if self.player_score >= 1000 and self.cpu_score >= 1000:
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')

        elif self.player_score >= 1000 and self.cpu_score < 10:
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')

        elif self.player_score >= 1000 and self.cpu_score >= 10:
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')

        elif self.cpu_score >= 1000 and self.player_score >= 100:
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')

        elif self.cpu_score >= 1000 and self.player_score >= 10:
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')
            self.player_score_border.remove(' ')

        elif self.player_score >= 100 and self.cpu_score >= 100:
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')

        elif self.player_score >= 100 and self.cpu_score >= 10:
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')
            self.cpu_score_border.remove(' ')

        elif self.cpu_score >= 100 and self.player_score >= 10:
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')
            self.player_score_border.remove(' ')

        elif self.player_score >= 100 and self.cpu_score < 10:
            self.player_score_border.remove(' ')
            self.player_score_border.remove(' ')

        elif self.cpu_score >= 100 and self.player_score < 10:
            self.cpu_score_border.remove(' ')
            self.cpu_score_border.remove(' ')

        elif self.player_score >= 10 and self.cpu_score >= 10:
            self.player_score_border.remove(' ')
            self.cpu_score_border.remove(' ')

        elif self.player_score >= 10 and self.cpu_score < 10:
            self.player_score_border.remove(' ')

        elif self.cpu_score >= 10 and self.player_score < 10:
            self.cpu_score_border.remove(' ')

        print('**********SCOREBOARD**********')
        print('*              |             *')
        print('* ' + ' Player: ' + str(self.player_score) + ''.join(self.player_score_border) + '    ' + 'CPU: ' + str(self.cpu_score) + ''.join(self.cpu_score_border))
        print('*              |             *')
        print('******************************')

    def game_rules(self):
        print('Here are the rules:')
        print('Create a matching sequence of your shape to win.')
        print('The matching sequence can be horizontal, vertical, or diagonal.')
        if self.player_unit == 'X' and self.cpu_unit == 'O':
            print('You are X. The CPU will be O.')
        elif self.player_unit == 'O' and self.cpu_unit == 'X':
            print('You are O. The CPU will be X.')
        print('Select a number relative to the position you wish to base your next move.')

    def show_game_board(self):
        print('1' + ' | ' + '2' + ' | ' + '3' + '    ' + self.game_board[0] + ' | ' + self.game_board[1] + ' | ' + self.game_board[2])
        print('4' + ' | ' + '5' + ' | ' + '6' + '    ' + self.game_board[3] + ' | ' + self.game_board[4] + ' | ' + self.game_board[5])
        print('7' + ' | ' + '8' + ' | ' + '9' + '    ' + self.game_board[6] + ' | ' + self.game_board[7] + ' | ' + self.game_board[8])

    def check_for_win(self):
        if '-' not in self.game_board:
            print('Tie game!')
            tic_tac_toe.play_again()
            return

        if '-' in self.game_board:
            # Player win conditions
            # horizontal
            if self.player_unit in self.game_board[0] and self.player_unit in self.game_board[1] and self.player_unit in self.game_board[2]:
                print('You win!')
                self.player_score += 1
                tic_tac_toe.play_again()
                return

            if self.player_unit in self.game_board[3] and self.player_unit in self.game_board[4] and self.player_unit in self.game_board[5]:
                print('You win!')
                self.player_score += 1
                tic_tac_toe.play_again()
                return

            if self.player_unit in self.game_board[6] and self.player_unit in self.game_board[7] and self.player_unit in self.game_board[8]:
                print('You win!')
                self.player_score += 1
                tic_tac_toe.play_again()
                return

            # vertical
            if self.player_unit in self.game_board[0] and self.player_unit in self.game_board[3] and self.player_unit in self.game_board[6]:
                print('You win!')
                self.player_score += 1
                tic_tac_toe.play_again()
                return

            if self.player_unit in self.game_board[1] and self.player_unit in self.game_board[4] and self.player_unit in self.game_board[7]:
                print('You win!')
                self.player_score += 1
                tic_tac_toe.play_again()
                return

            if self.player_unit in self.game_board[2] and self.player_unit in self.game_board[5] and self.player_unit in self.game_board[8]:
                print('You win!')
                self.player_score += 1
                tic_tac_toe.play_again()
                return

            # diagonal
            if self.player_unit in self.game_board[0] and self.player_unit in self.game_board[4] and self.player_unit in self.game_board[8]:
                print('You win!')
                self.player_score += 1
                tic_tac_toe.play_again()
                return

            if self.player_unit in self.game_board[2] and self.player_unit in self.game_board[4] and self.player_unit in self.game_board[6]:
                print('You win!')
                self.player_score += 1
                tic_tac_toe.play_again()
                return

            # cpu win conditions
            # horizontal
            if self.cpu_unit in self.game_board[0] and self.cpu_unit in self.game_board[1] and self.cpu_unit in self.game_board[2]:
                print('CPU wins!')
                self.cpu_score += 1
                tic_tac_toe.play_again()
                return

            if self.cpu_unit in self.game_board[3] and self.cpu_unit in self.game_board[4] and self.cpu_unit in self.game_board[5]:
                print('CPU wins!')
                self.cpu_score += 1
                tic_tac_toe.play_again()
                return

            if self.cpu_unit in self.game_board[6] and self.cpu_unit in self.game_board[7] and self.cpu_unit in self.game_board[8]:
                print('CPU wins!')
                self.cpu_score += 1
                tic_tac_toe.play_again()
                return

            # vertical
            if self.cpu_unit in self.game_board[0] and self.cpu_unit in self.game_board[3] and self.cpu_unit in self.game_board[6]:
                print('CPU wins!')
                self.cpu_score += 1
                tic_tac_toe.play_again()
                return

            if self.cpu_unit in self.game_board[1] and self.cpu_unit in self.game_board[4] and self.cpu_unit in self.game_board[7]:
                print('CPU wins!')
                self.cpu_score += 1
                tic_tac_toe.play_again()
                return

            if self.cpu_unit in self.game_board[2] and self.cpu_unit in self.game_board[5] and self.cpu_unit in self.game_board[8]:
                print('CPU wins!')
                self.cpu_score += 1
                tic_tac_toe.play_again()
                return

            # diagonal
            if self.cpu_unit in self.game_board[0] and self.cpu_unit in self.game_board[4] and self.cpu_unit in self.game_board[8]:
                print('CPU wins!')
                self.cpu_score += 1
                tic_tac_toe.play_again()
                return

            if self.cpu_unit in self.game_board[2] and self.cpu_unit in self.game_board[4] and self.cpu_unit in self.game_board[6]:
                print('CPU wins!')
                self.cpu_score += 1
                tic_tac_toe.play_again()
                return

    def announce_player_turn(self):
        print('*****YOUR TURN*****')

    def announce_cpu_turn(self):
        print('*****CPU\'S TURN*****')

    def player_turn(self):
        self.player_choice = int(input('Select a position: '))
        if self.player_choice not in range(1,10):
            print('That was not a valid choice. Try again.')
            tic_tac_toe.player_turn()
        if self.game_board[self.player_choice-1] == '-':
            self.game_board[self.player_choice-1] = self.player_unit
            print('The player has selected ' + str(self.player_choice) + '!')
            return
        else:
            print('That spot is already taken. Please try again.')
            tic_tac_toe.player_turn()
            return
        return

    def cpu_turn(self):
        self.cpu_choice = random.randint(0,8) #randint includes both endpoints (a,b)
        if '-' in self.game_board:
            if self.game_board[self.cpu_choice] == '-':
                self.game_board[self.cpu_choice] = self.cpu_unit
                print('The CPU has selected ' + str(self.cpu_choice+1) + '!')
                return
            else:
                tic_tac_toe.cpu_turn()
        else:
            tic_tac_toe.check_for_win()
            return

    def play_again(self):
        tic_tac_toe.game_score()
        print('Play again? [Y]es or [N]o')
        replay = input('')
        if replay.upper() == 'Y':
            self.game_board = ['-','-','-','-','-','-','-','-','-']
            tic_tac_toe.game_setup()
            tic_tac_toe.game_loop()
            return
        elif replay.upper() == 'N':
            self.game_active = False
            print('Goodbye!')
            sys.exit()
        else:
            print('That was not a valid response. Try again.')
            tic_tac_toe.play_again()
            return

    def game_loop(self):
        while self.game_active == True:
            tic_tac_toe.show_game_board()
            tic_tac_toe.check_for_win()
            tic_tac_toe.announce_player_turn()
            tic_tac_toe.player_turn()
            tic_tac_toe.show_game_board()
            tic_tac_toe.check_for_win()
            tic_tac_toe.announce_cpu_turn()
            tic_tac_toe.cpu_turn()
tic_tac_toe = tic_tac_toe()
tic_tac_toe.game_setup()
tic_tac_toe.game_rules()
tic_tac_toe.game_loop()
