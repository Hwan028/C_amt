1~100까지의 수 중에서 15의 배수 출력



```c
#include <stdio.h>

int main(void) {
  int i=1;
  while(i<=100)
    {
      if(i%3==0&&i%5==0)
      {
        printf("%d,",i);
      }
      i++;
    }
  return 0;
}
