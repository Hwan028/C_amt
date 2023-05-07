구구단 출력



```c
#include <stdio.h>

int main(void) {
  int i=1,n;
  printf("보고 싶은 단은? : \n");
  scanf("%d",&n);
  while(i<=9)
    {
      printf("%d X %d = %d \n",n,i,n*i);
      i++;
    }
  return 0;
}
