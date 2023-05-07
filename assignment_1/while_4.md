입력받은 팩토리얼값의 출력



```c
#include <stdio.h>

int main(void) {
  int i=1,n;
  long long factorial=1;
  printf("구하고 싶은 팩토리얼의 값은?\n");
  scanf("%d",&n);
  while(i<=n)
    {
      factorial*=i;
      i++;
    }
  printf("%d!의 값은 %lld 입니다.",n,factorial);
  return 0;
}
