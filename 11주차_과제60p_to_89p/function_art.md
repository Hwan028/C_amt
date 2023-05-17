삼각함수 그리기



```c
#include <stdio.h>         //입출력 하기 위한 헤더 파일
#include <math.h>          //수학 공식 사용하기 위한 헤더 파일
#define PI 3.141592        //PI = 3.141592 라고 정의

double rad(double degree)  //라디안으로 바꾸는 사용자 정의 함수
  {
return PI * degree / 180.0;
  }

void drawbar(int height)
  {
for (int i = 0; i < height; i++)
printf("*");
printf("\n");
  }

int main(void)
{
int degree, x, y;
for (degree = 0; degree <= 90; degree += 10) 
  {
// 싸인값은 -1.0에서 1.0이므로 정수로 반올림하여서 증폭한다.
y = (int)(60 * sin(rad((double)degree)) + 0.5);
drawbar(y);
  }
return 0;
}
