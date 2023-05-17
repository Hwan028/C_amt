삼각함수 그리기 (sin90도~180도 까지를 그린듯)



```c
#include <stdio.h>         //입출력 하기 위한 헤더 파일
#include <math.h>          //수학 공식 사용하기 위한 헤더 파일
#define PI 3.141592        //PI = 3.141592 라고 정의

double rad(double degree)  //라디안으로 바꾸는 사용자 정의 함수
  {
  return PI * degree / 180.0;   //파이를 180도로 나누면 라디안이 됨
  }

void drawbar(int height)        //매개변수인 heihgt 값을 받아옴
  {
  for (int i = 0; i < height; i++)    //height값만큼 반복
  printf("*");                        //height값만큼 *을 찍음
  printf("\n");
  }

int main(void)
{
  int degree, x, y;           //정수형 변수 선언
  for (degree = 0; degree <= 90; degree += 10)    //9번 반복, degree는 10씩 증가함
    {
    y = (int)(60 * sin(rad((double)degree)) + 0.5);  //sin값을 계산후 60을 곱하고 0.5를 더하여 반올림을 한 정수를 y에 저장
    drawbar(y);           //y를 drawbar 함수에 넣어 y값 만큼 *찍음
    }
  return 0;         //정상 작동시 0을 출력
}
