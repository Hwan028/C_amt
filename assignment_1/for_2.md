1부터 입력한 수까지의 합



```c
#include <stdio.h>

int main(void) {
  int n,sum=0;
  printf("1부터 몇까지의 합을 알고싶은가요? \n");
  scanf("%d",&n);
  for(int i=1; i<=n; i++)
    {
      sum+=i;
    }
  printf("1부터 %d까지의 합은 %d 입니다. \n",n,sum);
  return 0;
}
