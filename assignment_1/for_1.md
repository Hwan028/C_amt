입력받은 단 출력 (구구단)



```c 
#include <stdio.h>

int main(void) {
  int n;
  printf("알고싶은 단은? :\n");
  scanf("%d",&n);
  
  for(int i=1; i<=9; i++)
    {
      printf("%d X %d = %d \n",n,i,n*i);
    }
  return 0;
}
