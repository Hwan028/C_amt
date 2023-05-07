입력한 수의 홀수,짝수 판별 (종료 : -1)



```c
#include <stdio.h>

int main(void) {
  for(int num; num!=-1; )
  {
      printf("판별할 숫자를 입력하시오 :\n");
      scanf("%d",&num);
    if(num!=-1)
    {
      if(num%2==1)
      {
        printf("입력하신 수 %d는 홀수 입니다. (종료=-1)\n\n",num);
      }
      else
      {
        printf("입력하신 수 %d는 짝수 입니다. (종료=-1)\n\n",num);  
      }
    }
    else
    {
    printf("종료");  
    }
  }
  return 0;
}
