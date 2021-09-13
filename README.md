MBC앱 4.1.1 업데이트
======
좀 된 이야기지만.. MBC앱을 업데이트 했다.
올림픽에 대응하기 위한 업데이트였고 여러 문제들을 해결했다.
입사한지 얼마 안되서 했던 작업이라 재밌게 했었다.
내가 작업한 내용을 기재한다.

## 1. 하단의 Bottom navigation 교체작업 (Material2의 BottomNavigationView를 사용)
기존에는 Custom된 하단 메뉴바를 사용하였는데 디자인 시안이 변경됨에 따라 그것들을 걷어내고 Matrial2의 BottomNavigationView를 적용하였다.
#### 기존의 하단 메뉴
![1](https://user-images.githubusercontent.com/64320373/133109401-29dda93a-ca53-46b0-9a44-34c71efe8f2e.png)
#### 변경된 하단 메뉴
![2](https://user-images.githubusercontent.com/64320373/133109411-dff336a6-e0e4-4682-bdfd-5b1ae6822245.png)

## 2. 홈 메뉴에 타임라인 구현 (WebView 처리 with JavascriptInterface, 다양한 기능이 동작하도록 구현)
홈 화면이 웹뷰로 구성됨에 따라 JavascriptInterface를 사용하여 기획서에 정의된 기능대로 동작하도록 구현
![3](https://user-images.githubusercontent.com/64320373/133109413-01af21c7-b110-4b8c-b189-272db164e11b.jpg){: width="300" height="300"){: .center}

## 3. 뉴스에 접근 시 Agent를 적용하여 구현 의도대로 화면이 구성되도록 구현
## 4. 온에어 탭에서 댓글 작성 시 영상 재생이 멈추던 현상 수정
Activity를 겹치던 구현 방식에서 DialogFragment로 교체하여 댓글을 작성하면서도 아래의 Activity가 멈추지 않도록 구현함
![4](https://user-images.githubusercontent.com/64320373/133108403-8efd5dcf-a951-4e19-8f10-070feacbb68b.jpg)
