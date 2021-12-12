# VIM PRACTICE 5일차

> 책 "손에 잡히는 VIM"의 5장 내용을 공부한 내용입니다. 이 문서는 5.1절만 정리합니다.

## 파일 열기

가령, `a.txt`를 작업 중에 2,4 라인을 복사하여 `b.txt`에다 붙여넣기를 하고 싶을 때 어떻게 해야할까요? `VIM`에서는 여러 창을 오가면서 이런 작업을 할 수 있습니다.

실습해봅시다. 먼저 [clientlist.txt](https://github.com/gurumee92/vim-practice/blob/main/src/day5/clientlist.txt)를 엽니다.

![01](./images/day5/01.png)

이제 여기서 2, 4번째 라인을 복사하기 위해 ":2,4y"를 입력합니다.

![02](./images/day5/02.png)

그 후 ":edit cp.txt"를 입력합니다.

![03](./images/day5/03.png)

그럼 새 창이 일반 모드로 실행됩니다. 여기에다 붙여넣기 기능인 "p"를 입력하면 다음과 같이 복사됩니다. 

![04](./images/day5/04.png)

여기서 만약 [clientlist.txt](https://github.com/gurumee92/vim-practice/blob/main/src/day5/clientlist.txt)로 돌아가고 싶다면 "ctrl + 6"을 입력하면 됩니다. (이 과정 이전에 [cp.txt](https://github.com/gurumee92/vim-practice/blob/main/src/day5/cp.txt)를 저장해야합니다.)

이번엔 한 번에 3개의 파일을 열어봅니다.

```bash
$ vim clientlist.txt cp.txt new.txt
```

이 때는 가장 첫 파일인 [clientlist.txt](https://github.com/gurumee92/vim-practice/blob/main/src/day5/clientlist.txt)가 열립니다. 이 때 다음 순서의 파일을 보고 싶다면 ":n"을 입력하면 됩니다.그럼 [cp.txt](https://github.com/gurumee92/vim-practice/blob/main/src/day5/cp.txt)로 이동하게 됩니다. 만약 이전 순서의 파일을 보고 싶다면 ":N"을 입력하면 됩니다.

만약 한 번에 연 파일을 모두 닫고 싶다면 ":q!"나 ":qa"를 입력해주면 됩니다.

