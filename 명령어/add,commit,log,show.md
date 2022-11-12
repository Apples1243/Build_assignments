# 명령어 정리
## 1. add
> ```git add```는 작업 디렉토리(WD)상의 변경 내용을 스테이징 영역(SA)에 추가하기 위해서 사용하는 Git 명령어입니다.
```git
git add 사용법 
$ git add <파일/디렉토리 경로>
```

> 아무것도 하지 않은 상태일 경우입니다.

![image](https://user-images.githubusercontent.com/110793635/201458033-3badfb2f-f731-4d5c-8014-65b772ec9522.png)
> 여기서 apple.py라는 파일을 만들고 ```git add```를 해봅니다.

![image](https://user-images.githubusercontent.com/110793635/201458093-c2847960-c785-4065-af7c-d0c0d815814a.png)
> 그다음 ```git status``` 명령어를 사용해봅니다.

![image](https://user-images.githubusercontent.com/110793635/201458133-df191a9f-1758-44f1-813e-063f65758567.png)
> 그러자 SA에 apple.py가 변경되었다면서 올라왔습니다.  
> 이렇게 WD의 변경 내용을 징검다리 역할을 하는 SA에 추가하는 명령어가 ```git add```입니다.

## 2. commit
> ```git add```로 SA에 추가한 내용을 Repository로 올리는 역할을 하는 것이 ```git commit```입니다.
```git
git commit 사용법
$ git commit <파일>
```
![image](https://user-images.githubusercontent.com/110793635/201458133-df191a9f-1758-44f1-813e-063f65758567.png)
> 전에 SA에 올려놨던 apple.py를 ```git commit```해봅니다.(-m을 사용하면 커밋 메시지를 적을 수 있습니다.)

![image](https://user-images.githubusercontent.com/110793635/201458377-81e7542c-a778-4d71-ab90-593d67d1c1a5.png)
> 그다음 ```status```와 ```log```를 확인해봅니다.  
> 그 결과 WD와 SA랑 Repository가 깨끗하다는 것을 알려주면서 log에는 commit한 결과가 나오는 것을 확인할 수 있었습니다.

## 3. log
> ```git commit```한 결과가 log에 남게 되는데 그 결과를 확인하기 위해 ```git log``` 명령어를 사용합니다.
```git
git log 사용법
$ git log <인자>
```
> ```git log```를 사용해 log를 확인해봅니다.

![image](https://user-images.githubusercontent.com/110793635/201458584-11fbe3d1-fb2a-4ea7-a199-ee769cc83917.png)
> 지금까지 했던 log의 결과가 나왔습니다.

## 4. show
> ```git log```와 비슷한 결과가 나오게 됩니다. log는 commit한 결과만 나타내지만 show는 전과 달라진 점이 무엇인지 알려줍니다.
```git
git show 사용법
$ git show <인자>
```

![image](https://user-images.githubusercontent.com/110793635/201458686-41d7b056-ab31-4bc4-a0fd-cd2eb350343e.png)
> ```git log```는 commit한 결과만 나타냈었지만 ```git show```는 위와 같이 변경된 점까지 보여줍니다.  
> 결과를 확인해보면 아무것도 없던 파일에 ```print('hello')``` 한 줄이 추가되었다는 것을 알려줍니다.
