공학용 계산기



```c
#include <stdio.h> //입출력을 위한 헤더 파일 포함시킴
#include <math.h>  //수학 공식을 사용하기 위한 헤더 파일 포함시킴

int menu(void)
{
    int n;                    //정수형 변수 n 선언
    printf("1.팩토리얼\n");   //메뉴들을 출력함
    printf("2.싸인\n");
    printf("3.로그(base 10)\n");
    printf("4.제곱근\n");
    printf("5.순열(nPr)\n");
    printf("6.조합(nCr)\n");
    printf("7.종료\n");
    printf("선택해주세요: ");
    scanf("%d", &n);      //n을 스캔 받음 &는 주소를 뜻함
    return n;             //n값을 반환 
}

void factorial()
{
    long long n, result = 1, i;    //값이 크니까 long long으로 변수를 선언해줌, n은 입려받으니 초기화 안함
    printf("정수를 입력하시오: ");
    scanf("%lld", &n);             //long long으로 변수를 선언하였으니 %lld로 받음
    for (i = 1; i <= n; i++)      //i=1로 초기화하고, n번 반복
        result = result * i;        // i++이라는 증감식으로 인해 계속 1씩 증가하는 i를 result에 n번 축적하여 곱해줌
    printf("결과 = %lld\n\n", result);    //결과 출력
}

void sine()   
{
    double a, result;               //소수점 때문에 더블로 선언
    printf("각도를 입력하시오: ");    
    scanf("%lf", &a);                 //더블로 선언 하였으니 %lf로 받음
    result = sin(a);                  //sin에 각도 a 를 넣어 계산한 뒤, result에 넣음 
    printf("결과 = %lf\n\n", result);   //결과 출력
}

void logBase10()
{
    double a, result;               //소수점 때문에 더블로 선언
    printf("실수값을 입력하시오: ");
    scanf("%lf", &a);               //더블로 선언 하였으니 %lf로 받음  
    if (a <= 0.0)                   //a 부분은 0보다 작으면 안됨 (수학적 오류) 0보다 작을시 오류 출력 
    {
        printf("오류\n");
    }
    else
    {
        result = log10(a);          //log 계산값을 result에 넣음
        printf("결과 = %lf\n\n", result);  //결과 출력
    }
}

int main(void)
{
    while (1)
    {
        switch (menu())       //메뉴를 실행하고 거기서 받아온 값을 switch에 넣어 케이스에 넣어줌
        {
        case 1:
            factorial();
            break;            //브레이크를 걸지 않을시 계속해서 실행되기에 브레이크를 해줌
        case 2:
            sine();
            break;
        case 3:
            logBase10();
            break;
        case 7:
            printf("종료합니다.\n");
            return 0;         //마지막이라서 브레이크 안해도 되는듯 함
        default:
            printf("잘못된 선택입니다.\n");
            break;
        }
    }
    return 0;   //정상 작동시 0 보냄
}
