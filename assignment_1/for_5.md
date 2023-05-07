입력받은 크기의 다이아 출력



```c
#include <stdio.h>

int main(void) {
  int size,i;
  printf("다이아의 크기를 입력하시오 : \n");
  scanf("%d",&size);
  for(int i=0; i<size; i++)                       //입력받은 수 만큼의 층 구축
    {
      for(int jump=0; jump<size-i; jump++)        //공백이 점점 줄어야하니 size에서 점점커지는 i를 빼주는걸 조건으로 세움
        {
          printf(" ");
        }
      for(int star=0; star<2*i+1; star++)         //별은 1부터 2개씩 늘어나니 (1,3,5...) 2*i+1를 조건으로 세움 ( 2*i-1은 i의 시작이 0이니 안됨 ) 
        {
          printf("*");
        }
      printf("\n");                               //위의 공백,별 for문이 실행 완료시 줄을 바꿔줌으로써 피라미드 형태를 만듬
    }                                               
                                                    //피라미드
  for(int star=0; star<2*size+1; star++)
    {
      printf("*");                                //중간줄을 따로 만들어줌
    }
  printf("\n");
  
  for(int i=size; i>0; i--)                       //입력받은 수 만큼의 층 구축
    {
      for(int jump=0; jump<=size-i; jump++)       //위와 반대로 공백이 점점 늘어나는 구조 size에서 점점 작아지는 i를 빼줌
        {
          printf(" ");
        }
      for(int star=0; star<2*i-1; star++)         //별은 2개씩 줄어드니 2*i-1을 조건으로 세움 ( 2*i+1은 마지막으로 되는 i가 1이므로 하면 마지막층이 별3개가 됨, 그러므로 안됨 )
        {
          printf("*");
        }
      printf("\n");                               //마찬가지로 위의 두개의 for문이 실행 완료시 줄을 바꿔줌으로써 역피라미드 형태를 만듬 
    }
  return 0;                                         
}                                                   //다이아 
