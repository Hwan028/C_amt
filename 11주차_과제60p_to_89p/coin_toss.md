동전 던지기 게임


```c
#include <stdio.h>    // 입력,출력을 하기 위해 사용 (지금은 출력만 사용)
#include <stdlib.h>   /* srand 와 rand 함수를 사용하기 위해 사용 (srand는 시드를 설정, 그리고 그 시드값으로 rand가 난수를 생성함.
                       만약에 srand를 사용하지 않으면 똑같은 시드를 사용하여 똑같은 난수만 생성함) */
#include <time.h>       // 타임 함수를 쓰기 위해 사용 ( 현재 시간을 가져오는데 사용 )
int coin_toss(void);    // 메인함수 밑에 사용자 정의 함수를 만들었으므로 전처리 부분에 사용하여 메인 함수에 사용 가능하게 만들음 

int main(void)      
{
  int toss;         // 정수형 변수 선언
  int heads = 0;    // 정수형 변수 선언 0으로 초기화 한것은 입력 받는게 아니니까 쓰레기 값이 들어가는것을 막기 위해
  int tails = 0;
  srand((unsigned)time(NULL));           /* srand로 시드값을 설정하는데 안에 (unsigned)time(NULL)을 넣음으로써 현재 시간을 기반으로 설정함.
                                         (타임 함수에서 받은 값을 부호 없는 정수로 바꿔줌) */
  for (toss = 0; toss < 100; toss++)    
  {                                      
    if(coin_toss() == 1)      
    { heads++; }                          /* 동전 던지기 100번 반복하는 for문. 
    else                                  토스한 값이 1일시 앞면 값인 heads를 1올려줌, 토스한 값이 1이 아닐시 tails 값을 1 올려줌. */
    { tails++; }
  }
  printf("동전의 앞면: %d \n", heads);     //받은 값을 정수형으로 출력
  printf("동전의 뒷면: %d \n", tails);
  return 0;                                 //함수 잘 돌아갔으니 0 보내줌
}

int coin_toss( void )
{                                 /* 동전은 앞면, 뒷면 2가지니까 난수를 2로 나눈 나머지가 2개여야 하니,
  int head = rand() % 2;             rand()%2를 하여 0,1 두 수가 나올 수 있게 해줌. 그리고 헤드 값을 반환하여 줌 */
  return head;
}
