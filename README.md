# Tic-Tac-Toe
/*
* Name: Tic Tac Toe
* Program to create a basic Tic-Tac-Toe
* Start Date: 04/29/2022
* Author: Shadd Rivera
*/
#include "stdio.h"


/*
int board[25] = {
	:,:,:,:,:,
	:,O,-,X,:,
	:,X,-,-,:,
	:,-,-,-,:,
	:,:,:,:,:,
}
	*/

const int NOUGHTS = 1;
const int CROSSES = 2;
const int BORDER = 8;
const int EMPTY = 0;

const int ConvertTo25[9] = {
	6,7,8,
	11,12,13,
	16,17,18
};

void InitialiseBoard(int* board) {
	int index = 0;

	for (index = 0; index < 25; ++index) {
		board[index] = BORDER;
	}

	for (index = 0; index < 9; ++index) {
		board[ConvertTo25[index]] = EMPTY;
	}
}

void PrintBoard(const int* board) {
	int index = 0;
	printf("\nWelcome to my Tic-Tac-Toe Game\nBy: Shadd Rivera\n\n\nBoard:\n");
	for (index = 0; index < 25; ++index) {
		if (index != 0 && index % 5 == 0) {
			printf("\n");
		}
		printf("%4d", board[index]);
	}

}


int main() {


	int board[25];
	InitialiseBoard(&board[0]);
	PrintBoard(&board[0]);

	return 0;
}
