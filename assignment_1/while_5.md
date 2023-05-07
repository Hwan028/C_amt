  사용자로부터 계속해서 숫자를 입력받다가, -1을 입력받으면 입력받은 숫자들 중에서 짝수의 개수와 홀수의 개수를 출력



```c
#include <stdio.h>

int main(void) {
  int n,odd=0,even=0;
  while(n!=-1)
  {
    printf("숫자 입력(-1입력시 종료):");
    scanf("%d",&n);
    if(n%2==0)
    {
      even+=1;
    }
    else{
      odd+=1;
    }
  }
  odd--;
  printf("입력 받은 홀수의 개수: %d \n입력 받은 짝수의 개수: %d\n",odd,even);
  return 0;  
}
