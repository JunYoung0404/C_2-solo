1.리스트
--------
>리스트의 종류와 설명:

 1. Singly Linked List
 
 노드안에 링크가 1개이고
 
 단방향으로 진행하는 리스트
 
 2. Doubly Linked List
 
 노드안에 링크가 2개이고 양방향으로 
 
 진행할수있는 리스트
 
 3. Circular Linked List
 
 마지막 노드가 첫번째 노드를 가르켜서
 
 계속 회전할수있게 만들어진 리스트
 
>리스트 예제 코드

#include <stdio.h>

#include <stdlib.h>

typedef struct list {

 int d;

 struct list* p;

} LIST;

LIST* root = NULL;

LIST* last = NULL;

void AddList(int a){

 LIST* r = (LIST*)malloc(sizeof(LIST));

 r->d = a;

 r->p = NULL;

 if(root==NULL) root = r;

 else           last->p = r;

 last = r;

}

int main(void){

 AddList(35);

 AddList(40);

 AddList(45);

 while(root){

  printf("%d\n", root->d);

  root = root->p;
 }
}

>3.그림설명

저는 쉽게 이해하기 위해 그림을 그려보았습니다.
![KakaoTalk_20191109_024053608](https://user-images.githubusercontent.com/50895748/68498681-ce71b900-029a-11ea-995c-39bac098966a.jpg)


***
2.트리
------

>트리의 종류와 설명

1.이진트리 

차일드 노드가 최대 2개 까지 붙는 트리

2.터너리 트리 

노드에 차일드가 3개 붙까지 붙는 트리 

3.이진 검색트리 

그안에 데이터가 왼쪽 노드와 그 이하 차일드 노드들은 현재 노드보다 작아야되고

오른쪽 노드와 그이하 노드들은 현재 노드보다 커야되는 트리

4.발란스 

너무 치우쳐저 있지만 안으면 된다.

완전이진트리 : 모든 노드들이 레벨별로 왼쪽부터 체워져있는 트리

5.풀바이너리 트리 

하나의 차일드 노드가 하나도 없는 트리

6.펄펙 바이너리 트리 

양쪽으로 모든노드가 두개가 있고 레벨도 정확하게 딱 떨어지는 피라미드 모양의 트리

>트리 예제 코드

#include <stdlib.h>               /* malloc */

typedef struct Tree {

struct Tr* l, * r;

int d;

} T;

void print(T* p) {

printf("%d\n", p->d);

if (p->l) print(p->l);

if (p->r) print(p->r);

}

T* mem() {

T* p = (T*)malloc(sizeof(T));

p->l = p->r = NULL;

return(p);

}

int main(void) {

T* r, * r1, * r2, * l1;

l1 = (T*)mem(); l1->d = 3;

r2 = (T*)mem(); r2->d = 8;

r1 = (T*)mem(); r1->d = 7; r1->r = r2;

r = (T*)mem(); r->d = 5; r->l = l1;  r->r = r1;

print(r);

>그림 설명

![KakaoTalk_20191109_024250437](https://user-images.githubusercontent.com/50895748/68499716-36c19a00-029d-11ea-9801-413a7390040d.jpg)

***

3.그래프
--------

>그래프의 종류 및 설명

1.Directed 그래프

방향이 있는 그래프(자기자신을 가르킬수도 있음)

2.Undirected 그래프

방향이 없는 그래프(tree의 모양)

3.Cyclic 그래프 

노드들이 하나 이상의 사이클을 만드는경우의 그래프

4.Acyclic 그래프 

사이클이 하나도 없는 그래프

>그래프 그림 설명

![KakaoTalk_20191109_030859108](https://user-images.githubusercontent.com/50895748/68500343-d03d7b80-029e-11ea-88f4-632632f60935.jpg)

***
4.소감
------
처음 배운 것이라 생소했지만, 교수님이 수업 시간에 유튜브의 강의를 5분 정도 보여주셔서 조금 이해가 되었지만, 정확히는 몰랐다. 그래서 고민을 하고 있다가 교수님께서 친구들과 의논하고 상의해 보는 시간을 주셔서 친구들과 상의를 해보았다. 처음에는 친구가 말로 설명해 주어서 잘못 알아 들었는데 친구가 그림판을 이용하여 그림으로 설명해주니깐 바로바로 귀에 쏙쏙 들어왔다. 그리고 기숙사에 돌아와서 What is C 카페에 들어가서 교수님께서 수업 시간에 보여주셨던 유튜브를 다시 한번 보면서 복습해보았습니다. 리스트와 트리에 대해서는 잘 알아들었는데 그래프가 살짝 어려운 것 같다. 그리고 수업 시간 때 교수님께서 보여주셧던 깃허브 마크다운을 기숙사에 가서 살펴보았는데 엄청나게 유용했습니다. 내 깃허브를 더욱더 멋있게 꾸밀 수도 있을 것 같아 이번 과제에 적용해 보았다 글씨 크기 바꾸기, 사진넣어보기, 줄생기기 등등 새로운 깃허브 명령어들을 알게 되었으니 앞으로 과제를 할 때마다 사용해볼 것입니다. 깃허브를 생활화하여서 접속 횟수를 초록색 잔디밭으로 만들어볼 것입니다. C언어 화이팅!!!

