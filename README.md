# Practice-c-language- start 2022.11.02. 
# Gwangju Human Resources Development Center Professor Lee Sang-bok, Ryu Hong-geol Professor
![image](https://user-images.githubusercontent.com/115389450/233295913-579a37bf-ea5a-4b03-b1d0-4c2e06ac7e6d.png)

## 출석부
![image](https://user-images.githubusercontent.com/115389450/233290380-8d543f90-2603-43b2-ba6d-6dfb0330e808.png)

```
#include <stdio.h> // 기본 헤더 파일 선언

int main(void) // main 함수
{
/*
1. 우리반 학생 10명의 이름과 연락처를 조사하시오.
2. 과목은 국어 영어 수학 c언어 입니다.
3. 각 학생들의 c언어 점수는 사용자가 직접 입력합니다. (scanf)
4. c언어 점수는 조사한 연락처의 뒷번호 끝 두자리입니다. (단, 00은 100점으로 한다)
5. 우리반 학생들 10명의 국어,영어,수학,c언어 성적표를 아래의 예시에 맞게 출력하는 프로그램을 작성하시오.
*/
 int a,b,c,d,e,f,g,h,i,j; // 변수 선언
 printf("우리반 학생 10명의 이름 : 정연호,임성경,김명은,임홍선,노도현,김기태,김성일,박규환,이범규,김재일\n");
 printf("각 학생들의 c언어 점수는 연락처 뒷번호 끝 두자리입니다.\n");
 printf("위에 적은 이름 순서대로의 연락처 뒷 2자리 : 92,82,89,23,69,03,63,06,80,78\n");
 printf("위에 적은 이름 순서대로의 c언어 성적(스페이스 공백 입력) : ");
 scanf("%d %d %d %d %d %d %d %d %d %d", &a, &b, &c, &d, &e, &f, &g, &h, &i, &j);

 printf("%18s %4s %4s\n", "성", "적", "표"); // %s는 문자열을 나타내고, 앞의 숫자는 필드 폭을 숫자칸만큼 확보하는 의미입니다.
 printf("______________________________________________\n"); 
 printf("%15s %5s %5s %7s %5s\n","국어", "영어", "수학", "c언어", "평균");
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "정연호", 100, 100, 100, a, (300+a)/4.0); // %f는 소수점을 나타내고, 예를 들어 0.1f를 치면 0.1의 자리까지 표현이 됩니다.
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "임성경", 100, 100, 100, b, (300+b)/4.0); // 필드 폭을 8칸 확보하고, 왼쪽 정렬해서 출력을 진행한다.
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "김명은", 100, 100, 100, c, (300+c)/4.0);
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "임홍선", 100, 100, 100, d, (300+d)/4.0);
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "노도현", 100, 100, 100, e, (300+e)/4.0);
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "김기태", 100, 100, 100, f, (300+f)/4.0);
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "김성일", 100, 100, 100, g, (300+g)/4.0);
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "박규환", 100, 100, 100, h, (300+h)/4.0);
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "이범규", 100, 100, 100, i, (300+i)/4.0);
 printf("%-8s %5d %5d %5d %7d %8.1f \n", "김재일", 100, 100, 100, j, (300+j)/4.0);
 printf("%-8s %6.1f %5.1f %4.1f %8.1f \n", "평  균", 100.0, 100.0, 100.0, (a+b+c+d+e+f+g+h+i+j)/10.0);
 printf("______________________________________________\n");

  return 0;
}
```
![image](https://user-images.githubusercontent.com/115389450/233291236-7b50db30-a048-4bb4-9484-6cc6e471dd56.png)
```
문제를 보고 어떤걸 요구하는지 파악을 해야할 것 같다.

그리고 최대한 표현하는 것에 집중을 해야할 것 같다.

범규형의 도움을 받아 표현하는 방식에 도움을 받았다.

그리고 한줄한줄씩 이해하려고 노력하고 직접 작성해보았다.

혼자서 하는 연습을 해야할 것 같다.

조금씩.. 앞으로 !~~
```
- - -
## 문제 2.아래의 출력을 보이는 프로그램을 작성해보자.
*

o*

oo*

ooo*

oooo*

참고로 총 5행에 걸쳐서 출력이 이뤄지고,

행이 더해질 때마다 o 문자의 수가 증가한다는 특징을 기반으로

while문의 중첩을 구성하면 된다.
- - -
```
#include <stdio.h> // 헤더 선언

int main(void) // main 함수 선언
{
 int i=0, k=0; // 변수 i, k 선언 및 값 지정,
 while(i<5) // 반복문 시작. 
 {
    while(k<i) 
    {
     printf("o"); 
     k++; 
    }
    k=0;  
    printf("*\n"); 
    i++; 
}
 return 0;
}
```
- - -
문제3.

별5개 ··· 별 1개 콘솔창 출력 
- - -
```
#include <stdio.h>

int main(void)
{
 int i=0,j=0;
 while(i<5)
 {
  while(j<5-i)
  {
   printf("*");
   j++;
  }
 printf("\n);
 j=0;
 i++;
 }
return 0;
}
```
![image](https://user-images.githubusercontent.com/115389450/233295040-f6162545-5faa-46aa-99e4-14fd180c3e53.png)

---
﻿
문제 2,3번을 풀고 깨달은 점

: 반복문에 대한 이해. 즉. 변수 값지정이 중요한 것을 깨달았다.

변수 값이 제대로 지정되있지 않으면, 반복이 제대로 이루어지지 않는다.

순서대로 차분히 진행되는데, 이 순서도를 머리에 그리지 못해서 코드를 짜지 못했다.

---
---
문제4.

별로 만들어진 피라미드 콘솔창 출력 
---
```
#include <stdio.h>

int main(void)
{
 int i,j,k;
 for(i=0; i<5; i++)
 {
  for(j=0; j<5-i; j++)
   {
    printf(" ");
   }
  for(k=0; k<i*2+1; k++)
  {
   printf("*");
  }
  printf("\n");
 }
 return 0;
}
```
![image](https://user-images.githubusercontent.com/115389450/233294081-c66483cb-95dd-4b68-9cfc-2209bff97a08.png)
---
문제 4번 피라미드 뒤집어 보기
---
```
#include <stdio.h>
int main(void)
{
 int i,j,k;
 for(i=0; i<5; i++)
 {
  for(j=0; j<i; j++)
  {
   printf(" ");
  }
  for(k=0; k<(5-i)*2-1; k++)
 {
  printf("*");
 }
  printf("\n")
 }
return 0;
}
```
![image](https://user-images.githubusercontent.com/115389450/233294694-faf8128f-47ab-4663-95c3-b2c854e5d672.png)
- - -
![image](https://user-images.githubusercontent.com/115389450/233295363-75314e6e-5500-4937-abc2-26bc6abc7cf1.png)
- - -
```
#include <stdio.h>

int main(void)
{
  int i,j,k;
  for(i=0; i<4; i++)
  {
    for(j=0; j<4-i; j++)
    {
      printf(" ");
    }
    for(k=0; k<i*2+1; k++)
    {
      printf("*");
    }
    printf("\n");
  }
  for(i=0; i<5; i++)
  {
    for(j=0; j<i; j++)
    {
      printf(" ");
    }
    for(k=0; k<(5-i)*2-1; k++)
    {
      printf("*");
    }
    printf("\n");
  }
  return 0;
}
```
- - -
![image](https://user-images.githubusercontent.com/115389450/233295552-998be15e-ce9d-4fda-903e-9275a194ee36.png)
- - -
```
#include <stdio.h>
int main(void)
{
  int i,j,k;
  for(i=0; i<7; i++)
  {
    for(j=0; j<i; j++)
    {
      printf(" ");
    }
    for(k=0; k<(7-i)*2-1; k++)
    {
      printf("*");
    }
    printf("\n");
  }
  for(i=0; i<7; i++)
  {
    for(j=0; j<6-i; j++)
    {
      printf(" ");
    }
    for(k=0; k<2*i+1; k++)
    {
      printf("*");
    }
    printf("\n");
  }
}
```
- - -
﻿
나눠서 생각해야한다.

문제가 크고 거대할지라도

하나하나씩 단계별로 나아가야한다

﻿
- - -
