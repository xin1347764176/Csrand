# Csrand
srand switch


#define _CRT_SECURE_NO_WARNINGS 1
#include <stdio.h>
#include <time.h>
#include <stdlib.h>
int game() {
	int guess; int a_time;
	a_time = rand() % 100 + 1;
	printf("%d\n", a_time);
	printf("input your guess\n");
	

		do {
			scanf("%d", &guess);
			if (guess == a_time)
				printf("yes\n");
			else if (guess > a_time) {
				printf("big\n");
			}
			else printf("small\n");
		} while (guess != a_time);//u can use 'break'

}


int main() {
	int choose=1;
	
	srand((unsigned)time(NULL));
	

	
		while (choose) {
			printf("play game?1or0\n");
			scanf("%d", &choose);
			switch (choose) {
			case 1:game();
				break;
			case 0:
				
				break;
			default:printf("wrong choice\n");
			}
		}
		return 0;
}

