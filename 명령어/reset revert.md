# reset , revert
## 1. reset
> 커밋 이력 재설정

```git
git reset 사용법
$ git reset <옵션> <돌아가고 싶은 커밋>
```
### reset의 옵션 3가지 <sup>[출처](#footnote_1)</sup>
- soft
- mixed
- hard

#### 1. soft
> reset 이후에 커밋 내용만 수정되고 WD와 SA는 이전과 같음
#### 2. mixed (생략 가능)
> reset 이후에 커밋 내용과 SA가 같음
#### 3. hard
> reset 이후에 커밋 내용으로 WD와 SA 모두 동일

![image](https://user-images.githubusercontent.com/110793635/204524415-04246373-8608-43e7-a793-9e409fa99d67.png)
![image](https://user-images.githubusercontent.com/110793635/204524473-f0591c68-3553-46a9-b454-ea3332c47d97.png)

#### reset 이후에 다시 이전 상태로 돌아가기
```$ git reset --hard ORIG_HEAD```를 사용한다.

## 2.revert
> 이전 로그를 남기고 새로운 커밋으로 커밋 되돌리기

> 취소, undo 수행
- 지정한 커밋을 취소해 바로 이전 상태로 되돌리는 방법
  - 커밋해온 모든 변경 사항들을 롤백
  - 이전의 커밋 히스토리는 그대로 유지되며, 이것을 되돌리는 새로운 커밋이 그 이후에 추가
![image](https://user-images.githubusercontent.com/110793635/204525156-6f046173-3cbd-4001-89ea-1d50f9f8a288.png)

- 현재 HEAD를 특정 시점 commit 이전 상태로 변경
> ```$ git revert <커밋 id>```
- <커밋 id> 바로 이전으로 이동
  - commit을 추가로 수행
  - 커밋 메시지 입력 편집기 실행
    - 기본 메시지 : 'revert 이전_메시지'
  - 과거의 모든 커밋은 그대로 유지
  - 새로운 커밋을 추가해 특정 시점 <커밋 id> 이전으로 이동

![image](https://user-images.githubusercontent.com/110793635/204525762-b35aa1e0-c0c2-4ef5-98b5-fa0c5ee25181.png)

## reset과 revert 비교
* 재지정과 취소

![image](https://user-images.githubusercontent.com/110793635/204525961-92c04431-3708-49fa-92fb-572a0bfd4005.png)
- reset은 되돌리는 이후 커밋 이력이 제거된다.
- revert는 현재까지의 커밋 이력에 되돌리기 커밋이 추가된다.

<a name="footnote_1">출처</a>: https://github.com/ai7dnn/OSS-lect
