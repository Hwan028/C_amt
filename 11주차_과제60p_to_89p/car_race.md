자동차 경주 게임



```c
#include <stdio.h>   //입출력 함수 사용하기 위해 사용
#include <stdlib.h>  //srand 와 rand 함수를 사용하기 위해 사용 (난수)
#include <time.h>    //time 함수를 사용하기 위해 사용
#include <conio.h>   //_getch() 함수를 사용하기 위해 사용 ( 하나의 문자를 입력받아 반환함. 사용자가 키를 누를 때까지 프로그램이 대기하고, 입력된 키를 바로 반환함 )

void disp_car(int car_number, int distance)  //자동차의 번호와 거리를 받아 출력하는 함수
{
    int i;                                   //정수 선언
    printf("CAR #%d:", car_number);          //차의 번호를 출력 ( CAR#1 이런식으로 )
    for( i = 0; i < distance/10; i++ )       //거리를 10으로 나눈 수 만큼 반복
    {
    printf("*");                             //자동차의 거리에 비례하여 * 출력
    }
    printf("\n");                            // 줄 넘김
}

int main(void)
{ 
    int i;                                   //정수 선언
    int car1_dist=0, car2_dist=0;            //정수 선언, 입력 받는 값이 아니니 쓰레기값 방지를 위해 0으로 초기화
    srand( (unsigned)time( NULL ) );         //부호가 없는 현재 시간을 기반으로 시드값을 생성함
    for( i = 0; i < 6; i++ )                 //6번 반복하는 FOR문
    {
    car1_dist += rand() % 100;               //0부터99까지의 난수를 각각의 차의 거리에 6번 축적시킴
    car2_dist += rand() % 100;
    disp_car(1, car1_dist);                  //함수를 호출하여 자동차의 번호와 이동한 거리를 출력함 ( 총 6번 함 )
    disp_car(2, car2_dist);
    printf("---------------------\n");       //위의 문장들이 출력되면 선을그어주고 다음줄로 넘어감( 진행 과정을 보여줌 )
    _getch();                                //키보드에서 사용자의 입력을 기다리는 함수로 사용자가 키를 누를 때까지 멈춰있다 누르면 작동( 입력값 반환 x )
    }
  return 0;                                  //정상 작동 했으니 0보냄
}
