## 1. branch
### 브랜치란
> 독립적으로 어떤 작업을 진행하기 위한 개념

> ```git branch``` 저장소 목록 보기

![image](https://user-images.githubusercontent.com/110793635/204514654-c2a484ad-b217-4703-be4f-87326d47bd23.png)
> ```git branch -a``` 저장소 목록 전체 보기 (원격 저장소 포함)

![image](https://user-images.githubusercontent.com/110793635/204514750-cd0f4c3c-6548-4c02-8310-095a7833d39e.png)
> ```git branch <브랜치 이름>``` 저장소 생성만

![image](https://user-images.githubusercontent.com/110793635/204514973-5a63f151-8083-44cc-9a43-0606b5bf3278.png)
> ```git branch -d , -D <브랜치 이름>``` 저장소 삭제 , -D는 강제 삭제

![image](https://user-images.githubusercontent.com/110793635/204515114-f7bf4bdd-ba50-404d-8e03-2144b7d9a8f7.png)

## 2. switch
> ```git switch -c <브랜치 이름>``` 저장소 생성 및 이동

![image](https://user-images.githubusercontent.com/110793635/204515308-5d730ecc-a7ee-4cd4-bf47-8810d3401e64.png)
> ```git switch <브랜치 이름>``` 전환 및 이동

![image](https://user-images.githubusercontent.com/110793635/204515424-c706603e-1d78-418b-aa76-8ee4d5976ee5.png)
> ```git switch -``` 이전 브랜치 전환 및 이동

![image](https://user-images.githubusercontent.com/110793635/204515522-64d31482-0308-4d4a-8145-e43d28d2c6be.png)

## 3. checkout
> ```git checkout -b <브랜치 이름>``` 저장소 생성 및 이동

![image](https://user-images.githubusercontent.com/110793635/204515682-b5dd72af-d076-43dc-a4c6-ba7150b8f098.png)
> ```git checkout <브랜치 이름>``` 전환 및 이동

![image](https://user-images.githubusercontent.com/110793635/204515802-7de4aa92-efce-4c33-8a9e-df7b0d383b7a.png)
> ```git checkout -``` 이전 브랜치 전환 및 이동

![image](https://user-images.githubusercontent.com/110793635/204515888-52eab104-a29e-4601-b1be-26b4e3bb0f8d.png)
> ```git checkout HEAD~``` HEAD 이전 커밋으로 이동 (detached head상태)

![image](https://user-images.githubusercontent.com/110793635/204516482-acb26137-a43b-43fd-9515-2a8741f1e2e4.png)
