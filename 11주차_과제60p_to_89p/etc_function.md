기타 함수 exit,system,time(NULL)



```c
#include <stdlib.h>  //time함수를 쓰기 위해 사용
#include <stdio.h>   //출력하기 위해 사용

int main(void)          
{
    system("dir");      //dir은 현재 디렉토리의 파일 및 폴더 목록을 출력함
    printf("아무 키나 치세요\n");
    _getch();             //키보드로부터 입력 받을때까지 기다렸다가 입력 받을시 진행시킴 ( conio.h 없이 사용 가능한지 모르겠음 )
    system("cls");        //cls는 명령을 실행하여 화면을 지우고, 프로그램이 종료시킴
   return 0;
}
//시스템 함수는 운영 체제의 명령 프롬프트에게 명령어를 전달하여 실행시키는 함수
