# 題目連結
https://www.geeksforgeeks.org/output-of-programs-set-4/?ref=lbp

<br/>

# Q1 Predict the output of below programs 

```
#include‹stdio.h›
int main()
{
	struct site
	{
		char name[] = "GeeksforGeeks";
		int no_of_pages = 200;
	};
	struct site *ptr;
	printf("%d",ptr->no_of_pages);
	printf("%s",ptr->name);
	getchar();
	return 0;
}
```
Ans:

Compiler error，因為 struct site *ptr 這有錯，

When you declare a structure, you actually declare a new data type suitable for your purpose. 

So you cannot initialize values as it is not a variable declaration but a data type declaration.


<br/>

# Q2 

```
int main()
{
	char a[2][3][3] = {'g','e','e','k','s','f','o',
						'r','g','e','e','k','s'};
	printf("%s ", **a);
	getchar();
	return 0;
}
```
Ans:

geeksforgeeks

只有初始化13個，剩下的皆為'\0'



<br/>

# Q3 

```
int main()
{
    char str[]= "geeks\nforgeeks";
    char *ptr1, *ptr2;
        
    ptr1 = &str[3];
    ptr2 = str + 5;
    printf("%c", ++*str - --*ptr1 + *ptr2 + 2);
    printf("%s", str);

    getchar();
    return 0;
}
```
Ans:

Explanation: 

Initially ptr1 points to ‘k’ and ptr2 points to ‘\n’ in “geeks\nforgeeks”. 

In print statement value at str is incremented by 1 and value at ptr1 is decremented by 1. So string becomes “heejs\nforgeeks” . 

First print statement becomes 

printf(“%c”, ‘h’ – ‘j’ + ‘\n’ + 2)

‘h’ – ‘j’ + ‘\n’ + 2 = -2 + ‘\n’ + 2 = ‘\n’

First print statements newline character. and next print statement prints “heejs\nforgeeks”. 

<br/>

# Q4 
```
#include <stdio.h>
int fun(int n)
{
	int i, j, sum = 0;
	for(i = 1;i<=n;i++)
		for(j=i;j<=i;j++)
			sum=sum+j;
	return(sum);
}

int main()
{
	printf("%d", fun(15));
	getchar();
	return 0;
}
```
<br/>

Ans:

Explanation: fun(n) calculates sum of first n integers or we can say it returns n(n+1)/2.


# Q5

```
#include <stdio.h>
int main()
{
	int c = 5, no = 1000;
	do {
		no /= c;
	} while(c--);

	printf ("%d\n", no);
	return 0;
}
```

Ans:

當c=0 時，執行下一次迴圈內部 會除與0，因此會報出error


<br/>




