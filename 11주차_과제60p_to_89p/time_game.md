시간 맞추기 게임



```c
#include <stdio.h>          //출력을 하기 위해 사용
#include <time.h>           //time 함수를 쓰기 위해 사용

int main(void)
{
    time_t start, end;              // time_t는 unsigned long과 동일함( start와 end 선언 )
    start = time(NULL);             //현재 시간을 start에 저장함 (time(NULL) 함수는 1970년 1월 1일부터 현재까지의 시간을 초 단위로 반환함)
    printf("10초가 되면 아무 키나 누르세요\n");
    while (1)                       // getchar()로 아무거나 입력받을시 중단함
  {
    if (getchar())
    break;
  }
    printf("종료되었습니다.\n");
    end = time(NULL);       //현재 시간을 end에 저장함
    printf("경과된 시간은 %ld 초입니다. \n", end - start); //end에서 start를 빼서 경과된 시간을 구함
   return 0;                  //정상 작동 했음으로 0 보냄
}
