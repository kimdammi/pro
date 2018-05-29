#include <stdio.h>

int countDigits(int n, int d);

int main()
{
	int num, digit, result;
	printf("자연수 입력 : ");
	scanf("%d", &num);
	printf("한자리 수 입력 : ");
	scanf("%d", &digit);

	result = countDigits(num, digit);

	printf("%d에는 %d가 %d번 나옵니다.\n", num, digit, result);

	return 0;
}

int countDigits(int n, int d)
{
	if(n=0 || n<0)
		return 0;

	else
	{

		int k,t;
		t=0;

		do
		{
			k=n%10;

			if (k=d)
				t++;

			n = n/10;
		}while(n<0);

		return t;

	}
}
