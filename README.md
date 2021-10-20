
/*A basic calculator program design by matthew & walter*/
#include<stdio.h>

int main()
{
    /*variable declarations*/
	double matt, walter;
	int partner;

	/*printing welcome text,designer's names and board.*/
	printf("\n\n 	******Welcome!******\n\n");
	printf("     Basic Calculator by Matt & Walter\n\n\n");
	printf("    |------|-------|------|------|\n");
	printf("    |   1  |   2   |   3  |   /  |\n");
	printf("    |______|_______|______|______|\n");
	printf("    |      |       |      |      |\n");
	printf("    |   4  |   5   |   6  |   -  |\n");
	printf("    |______|_______|______|______|\n");
	printf("    |      |       |      |      |\n");
	printf("    |   7  |   8   |   9  |   +  |\n");
	printf("    |______|_______|______|______|\n");
	printf("    |      |       |      |      |\n");
	printf("    |      |   0   |   .  |   =  |\n");
	printf("    |______|_______|______|______|\n");

	/*printing operator selections and getting user's choice*/
	printf("\nOperators:\n1.Addition( + )\n2.Subtraction( - )\n3.Multiplication( * )\n4.Division( / )\n");
	printf("\nEnter number (1-4) for operator: ");
	scanf("%d", &partner);

	if(partner > 4)
	{
		printf("\nInvalid Selection!\n"); //if user's choice is true, execute if statement and default case.
	}
	else
	{
		printf("\nEnter TWO Numbers: "); //if user's choice false, then execute else statement and proceed to switch statement
		scanf("%lf %lf", &matt, &walter);
    }

	switch (partner)
	{
		case 1: printf("%.2lf + %.2lf = %.2lf\n", matt, walter, (matt+walter));
		break;

		case 2: printf("%.2lf - %.2lf = %.2lf\n", matt, walter, (matt-walter));
		break;

		case 3: printf("%.2lf * %.2lf = %.2lf\n", matt, walter, (matt*walter));
		break;

		case 4: if(walter !=0) //if variable walter is not equal to 0 execute if statement.
					printf("%.2lf / %.2lf = %.2lf\n", matt, walter, (matt/walter));
				else
					printf("Number cant be divided by 0\n");  // if variable walter is equal to 0 execute else statement
				break;

		default:printf("Please choose carefully!\n");
				break;
	}
	return 0;
}
