math 헤더 파일



```c
#include <math.h>
#include <stdio.h>

int main()
{
    double result, value = 1.6;
    result = floor(value);        // floor는 내림하는것 이므로 1.000000이 출력됨 ( lf으로 받아서 소수점 )
    printf("%lf \n", result);
    result = ceil(value);         // ceil은 올림하는것 이므로 2.000000이 출력됨 ( lf으로 받아서 소수점 ) 
    printf("%lf \n", result);
    
    printf("12.0의 절대값은 %f\n", fabs(12.0));  //fabs는 절댓값을 하는것 이므로 -가 없어진 값을 출력 
    printf("-12.0의 절대값은 %f\n", fabs(-12.0));
    
    printf("10의 3승은 %.0f.\n", pow(10.0, 3.0)); //pow는 n제곱을 해주는것 이므로 앞의것의 뒤의수만큼 제곱해줌 ( %.0f 이므로 소수 0번째까지 출력 )
    printf("16의 제곱근은 %.0f.\n", sqrt(64));    //sqrt는 무엇을 제곱하면 입력받은 값이 나오는지 알려주는것임 ( %.0f 이므로 소수 0번째까지 출력 )

    double pi = 3.1415926535;  //파이값 자리가 많이 필요하여 더블로 선언
    double x, y;
     x = pi / 2;                                //45도 라는 임의의 값
     y = sin( x );                              // 사인 pi / 2 값을 y에 저장
    printf( "sin( %f ) = %f\n", x, y );  
     y = cos( x );                              // 코사인 pi / 2 값을 y에 저장
    printf( "cos( %f ) = %f\n", x, y ); 
}
/* 중간 점검
1. x = sin( pi / 2 );
2. 0~9                */
