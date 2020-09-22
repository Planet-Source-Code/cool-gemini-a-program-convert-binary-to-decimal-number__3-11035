<div align="center">

## A Program Convert Binary to Decimal Number \]


</div>

### Description

Write a program to convert binary number to decimal number.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Cool\_Gemini](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/cool-gemini.md)
**Level**          |Beginner
**User Rating**    |4.0 (8 globes from 2 users)
**Compatibility**  |C, C\+\+ \(general\), UNIX C\+\+
**Category**       |[Algorithms](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/algorithms__3-29.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/cool-gemini-a-program-convert-binary-to-decimal-number__3-11035/archive/master.zip)





### Source Code

```

#include<stdio.h>
#include<conio.h>
#include<math.h>
int main(void)
{
 int i=0,j=0,sum=0,n,tmp,tmp1;
 long int arr[5];
 char pch;
 clrscr();
 printf("Enter binary number : ");
 while (scanf("%d",&n) != 1)
			 {
				while ((pch = getchar()) != '\n')
					  putchar(pch); // dispose of bad input
				 printf(" is not an binary number.\nPlease enter a ");
				 printf("binary value, such as 100, 1011, or 1111: ");
			 }
 while(n!=0)
	{
		arr[i]=n%10;
		n=(n-arr[i])/10;
		tmp=i;
		i++;
	}
 if(i>=5)
	{
		printf("\n\tNumber Out Of Range");
		getch();
		exit(0);
	}
 for(j=0;j<=tmp;j++)
	if(arr[j]!=1&&arr[j]!=0)
	{
		printf("Enter binary no. only");
		getch();
		exit(0);
	}
 tmp1=tmp;
 for(j=0;j<=tmp;j++)
	{
		sum=sum+(arr[j]*(pow(2,tmp1)));
		tmp1--;
	}
 printf("\nEquivalent decimal number is %d",sum);
getch();
return 0;
}
```

