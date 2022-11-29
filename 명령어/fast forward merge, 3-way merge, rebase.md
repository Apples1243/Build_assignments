# merge
> merge란 branch를 다른 branch로 합치는 과정을 merge라고 합니다. merge의 기본 단위는 branch이며, merge 명령어로는 커밋 단위로 합치기가 불가능합니다.

## 1. Fast Forward Merge
> 가장 기본적인 merge는 바로 Fast Forward merge입니다.  
> Fast Forward merge는 현재 브랜치의 HEAD가 대상 브랜치의 HEAD까지로 옮기는 merge입니다.

> 예를 들어 이러한 log가 있다고 합니다. <sup>[출처](#footnote_1)</sup>

![image](https://user-images.githubusercontent.com/110793635/204518474-a3b0dbbd-b9f6-402b-af6e-7424bbdec17f.png)
> 이를 그림으로 표현하면 다음과 같습니다.

![image](https://user-images.githubusercontent.com/110793635/204519197-b430a94b-6f9f-4566-b639-682dff790272.png)
> ```git merge feature-view```를 합니다. 그러자 main이 third branch로 옮겨지는 것을 알 수 있습니다.

![image](https://user-images.githubusercontent.com/110793635/204519390-dc995cfe-f42f-4987-9cc9-5d2e53033d2a.png)
> 이를 그림으로 표현하면 다음과 같습니다.

![image](https://user-images.githubusercontent.com/110793635/204519536-da692247-05d1-43b0-bd27-70bd4a1c6d35.png)

## 2. 3-way Merge
> 3-way Merge는 두 branch의 공통 조상 커밋을 찾아서 merge를 합니다.

> 예를 들어 이러한 그림이 있습니다.

![image](https://user-images.githubusercontent.com/110793635/204520033-01757dab-d915-4748-b586-f7deb564f63e.png)
> 여기서 git merge를 하게 되면 다음과 같습니다.

![image](https://user-images.githubusercontent.com/110793635/204520767-e8163bc1-ae72-4683-a5ea-ba4a25203143.png)
> 위 결과를 살펴보면 하나의 브랜치와 다른 브랜치의 모든 변경 이력을 합치는 방식으로 최종적으로 Merge commit이 새로 생성되고 2개의 부모를 가지게 됩니다.

## 3. rebase
> rebase는 FF , 3-way merge보다 조금 더 깨끗한 history를 만들 수 있습니다.

> 예를 들어 이러한 그림이 있습니다.

![image](https://user-images.githubusercontent.com/110793635/204521646-1ca97db3-745b-4fea-95f8-cee2fbc1ee92.png)
> 이렇게 나뉜 브랜치를 rebase를 통해 Merge합니다.
```git
$ git rebase master
```
![image](https://user-images.githubusercontent.com/110793635/204521835-7af2eebd-c9a3-4f7e-85bd-d18601928a5c.png)
> 그 결과 C5와 C4가 사라지고 C4`가 생겼습니다.  
> C4`의 변경사항을 C3에 적용합니다. (master 브랜치에서 FF merge)
```git
$ git checkout master
$ git merge experiment
```
![image](https://user-images.githubusercontent.com/110793635/204522065-671c41d9-bf76-42bc-9981-eecf43be80c3.png)
> 결과적으로 나눠졌던 브랜치가 선형으로 모든 작업이 차례대로 수행된 것처럼 보이게 됩니다.


<a name="footnote_1">출처 </a>: https://kotlinworld.com/277
