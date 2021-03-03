# Matrix_Calculate                      // FATIH TASTEKIN
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

#define      MAX_SIZE   100



int main() {

	int row1, col1,row2,col2;
	int Matrix[MAX_SIZE][MAX_SIZE] = { 0 };
	int Matrix1[MAX_SIZE][MAX_SIZE] = { 0 };
	int Matrix2[MAX_SIZE][MAX_SIZE] = { 0 };


	printf("Enter matrix of 1st row:  ");
	scanf("%d", &row1);
	printf("Enter matrix of 1st column: ");
	scanf("%d", &col1);

	for (int i = 0; i < row1; ++i) 
		for (int j = 0; j < col1; ++j) {
			printf("%d. row and  %d. column: ",i+1,j+1);
			scanf("%d", &Matrix[i][j]);
			
		}
	
	for (int i = 0; i < row1; ++i) {
		for (int j = 0; j < col1;++j)
			printf("%d\t", Matrix[i][j]);

			printf("\n");
	}



	printf("Enter matrix of 2nd row: ");
	scanf("%d", &row2);
	printf("Enter matrix of 2nd column: ");
	scanf("%d", &col2);


	for (int i = 0; i < row2; ++i)
		for (int j = 0; j < col2; ++j) {

			printf("%d. row and %d. column: ", i + 1, j + 1);
			scanf("%d", &Matrix1[i][j]);

		}

	for (int i = 0; i < row2; ++i) {
		for (int j = 0; j < col2; ++j)
			printf("%d\t", Matrix1[i][j]);

		printf("\n");
	}

	for(int i=0;i<row1;++i)
		for (int j = 0; j < col2; ++j) {
			int temp = 0;
			for(int k=0;k<col1;++k)
				temp += Matrix[i][k] * Matrix1[k][j];

			Matrix2[i][j] = temp;

		}



	for (int i = 0; i < row1; ++i) {
		for (int j = 0; j < col2; ++j)
			printf("%d\t", Matrix2[i][j]);

			printf("\n");
	}





}
