층을 입력받아 그 층 만큼의 크기를가진 직각삼각형 출력



```c
#include <stdio.h>

int main(void) {
  int num;
  printf("직각삼각형의 층을 입력하시오 : \n");
  scanf("%d",&num);
  for(int i=0; i<num; i++)                     //입력 받은 수 만큼의 층을 만들어줌
    {
      for(int j=0; j<num-i; j++)               //밑의 층으로 내려갈수록 띄어쓰기는 작아져야 함
        {
          printf(" ");
        }
      for(int s=0; s<=i; s++)                  //밑의 층으로 내려갈수록 별의 개수 증가
        {
          printf("*");
        }
      printf("\n");                            //삼각형을 만들어주기위해 띄어쓰기와 별 포문이 완료시 다음줄로 이동
    }
  return 0;                                    //정상작동 했다고 0을 반환
}
