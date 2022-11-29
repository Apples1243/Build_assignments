## 1. clone
> ```git clone```은 저장소를 복제하는 것입니다.
```git
git clone 사용법
$ git clone <url>
```
> 자신의 파일에 OSS-lect 복제하기

![image](https://user-images.githubusercontent.com/110793635/204499354-992aaa97-dc40-44d9-995b-ead0cb1cdd76.png)
> clone을 사용해 저장소를 복제합니다. 그 결과 OSS-lect라는 폴더가 생성되었으며 OSS-lect 폴더로 들어가보니 복제된 것을 확인할 수 있습니다.

## 2. push
> ```git push```는 원격 저장소에 코드 변경점을 업로드하기 위해서 사용하는 git 명령어입니다.
```git
git push 사용법
$ git push <저장소명> <브랜치명>
```
> ``` git clone```을 이용해 저장소를 복제했다면 ```git remote``` 명령어를 통해 정확한 저장소명을 알 수 있습니다.

>rpsync 저장소에 push하기

![image](https://user-images.githubusercontent.com/110793635/204501568-efb17255-c3e8-4013-8d80-2c55c9fad78f.png)  
![image](https://user-images.githubusercontent.com/110793635/204501683-b51778dd-599c-47d6-b7a0-3e8c25d70334.png)
> 그 다음 로그인까지 하게 되면 다음과 같이 됩니다.

![image](https://user-images.githubusercontent.com/110793635/204501916-cc4391bf-a310-4df8-b14a-3cf800bfdc54.png)
> 그러자 원격 저장소인 rpsync에는 test.py가 생성되었습니다.

![image](https://user-images.githubusercontent.com/110793635/204502144-981e1786-70ef-4728-b3b8-d8703f5da4c5.png)

## 3. pull
> ```git pull```은 원격 저장소의 변경점을 로컬 저장소에 옮겨와 병합하는 것입니다.
```git
git pull 사용법
$ git pull <저장소명> <브랜치명>
```
> rpsync 저장소에서 pull.md를 만든 뒤 로컬 저장소에서 pull을 합니다.

![image](https://user-images.githubusercontent.com/110793635/204506805-c59e9ac4-1c09-4a0b-a506-6fabc7b5b363.png)
> 그러자 자동으로 병합까지 된 것을 확인할 수 있습니다. 아래 사진을 통해 pull.md파일이 생긴 걸 확인할 수 있습니다.

![image](https://user-images.githubusercontent.com/110793635/204507006-a9056fdd-d217-4391-acd6-32ca9d744d3f.png)


## 4. fetch/merge
> ```git fetch```는 원격 저장소의 변경점을 로컬 저장소에 옮겨오기만 합니다.

```git
git fetch 사용법
$ git fetch <저장소명> <브랜치명>
```

> rpsync 저장소에서 fetch.md를 만든 뒤 로컬 저장소에서 fetch를 합니다.

![image](https://user-images.githubusercontent.com/110793635/204507609-3575eb50-50c2-4816-b8b3-1cb8dd15239d.png)
> 그 다음 ```git status``` 명령어를 사용해보니 1개의 commit이 있다는 것을 알려줍니다.  
> fetch는 merge가 되지 않은 상태이기 때문에 merge를 합니다. 그러자 FF 상태로 merge가 된 것을 확인할 수 있었습니다.

![image](https://user-images.githubusercontent.com/110793635/204508497-74ea3b69-188f-4749-b6d4-85905bcf32e6.png)
