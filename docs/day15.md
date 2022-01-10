# VIM PRACTICE 15일차

> 책 "손에 잡히는 VIM"의 8장 내용을 공부한 내용입니다. 이 문서는 8.2절만 정리합니다.

## 탭 대신 공백 사용하기

[예제 파일](https://github.com/gurumee92/vim-practice/blob/main/src/day15/ex01.c)를 열어보면 다음과 같다.

```c
#include<stdio.h>
int main(){
printf("hello\n");
return 0;
}
```

이런 코드는 가독성이 나쁘다. 정렬을 하고 싶다면 다음 옵션들을 생각해볼 수 있다.

* {visual block}=
* =G (일반모드)

`=G`를 했을 때 결과는 다음과 같다.

```c
#include<stdio.h>
int main(){
	printf("hello\n");
	return 0;
}
``` 

이 때 모두 탭이 들어간다. 근데 일반적으로 회사에는 코드 컨벤션이라는게 있다. 따라서 이 탭들을 빈칸으로 바꾸는 명령어도 알아보자. 

처음 상태로 되돌린 후, `:set et ts=4`를 입력한다. 그 후 다시 재정렬을 해보자. 그럼 다음과 같이 정렬이 된다.

```c
#include<stdio.h>
int main(){
        printf("hello\n");
        return 0;
}
```

위 결과의 차이점이 무엇일까? 공백칸을 지워보면 알 수 있다. 첫번째처럼 탭일 때는 `Backspace`를 누르면 빈공간이 사라진다. 두번째 `:set et` 옵션을 활성화시켰을 때는 모두 빈칸이기 때문에 한 칸만 뒤로 가는 것을 확인할 수 있다. 

참고로 모든 문서의 탭을 빈칸으로 혹은 빈칸을 탭으로 바꾸고 싶을 때는 `:ret` 명령어로 바꿀수 있다. `:set et` 옵션이 켜져있다면 탭을 공백으로, 꺼져있다면 공백을 탭으로 바꿔준다. 
![01](./images/day15/01.png)
