MBC앱 4.1.1 업데이트
======
좀 된 이야기지만.. MBC앱을 업데이트 했다.
올림픽에 대응하기 위한 업데이트였고 여러 문제들을 해결했다.
입사한지 얼마 안되서 했던 작업이라 재밌게 했었다.
내가 작업한 내용을 기재한다.

## 1. 하단의 Bottom navigation 교체작업 (Material2의 BottomNavigationView를 사용)
기존에는 Custom된 하단 메뉴바를 사용하였는데 디자인 시안이 변경됨에 따라 그것들을 걷어내고 Matrial2의 BottomNavigationView를 적용하였다.
#### 기존의 하단 메뉴
<img src="https://user-images.githubusercontent.com/64320373/133109401-29dda93a-ca53-46b0-9a44-34c71efe8f2e.png"></img>
#### 변경된 하단 메뉴
<img src="https://user-images.githubusercontent.com/64320373/133109411-dff336a6-e0e4-4682-bdfd-5b1ae6822245.png"></img>

## 2. 홈 메뉴에 타임라인 연동
홈 화면이 웹뷰로 구성됨에 따라 JavascriptInterface를 사용하여 기획서에 정의된 기능대로 동작하도록 구현

<img src="https://user-images.githubusercontent.com/64320373/133109413-01af21c7-b110-4b8c-b189-272db164e11b.jpg" width=30%></img>

## 3. 뉴스에 접근 시 Agent를 적용하여 구현 의도대로 화면이 구성되도록 구현
## 4. 온에어 탭에서 댓글 작성 시 영상 재생이 멈추던 현상 수정
Activity를 겹치던 구현 방식에서 DialogFragment로 교체하여 댓글을 작성하면서도 아래의 Activity가 멈추지 않도록 구현함

<img src="https://user-images.githubusercontent.com/64320373/133108403-8efd5dcf-a951-4e19-8f10-070feacbb68b.jpg" width=30%></img>
## 5. 다시보기 탭에서 지금무료 탭을 구현
item들이 순차적으로 Lazy loading 되도록 하고 좌측 상단에 무료라는 태그가 노출되도록 구현 좌측 무료 태그의 경우 drawable에 shape를 선언하여 만듬

<img src="https://user-images.githubusercontent.com/64320373/133108414-6d3684c4-32f1-4ede-82f7-27ad8fafd3a7.jpg" width=30%></img>

## 6. 음성 검색과 저장소 관련 권한 부여 로직 변경
기존에는 앱 최초 실행시 일괄적으로 권한을 부여 받는 형태였지만 https://developer.android.com/guide/topics/permissions/overview 에 워크플로우를 동일하게 구현하여 불필요한 권한 부여가 이루어지지 않도록 구현

<img src="https://user-images.githubusercontent.com/64320373/133108421-343240ef-f647-4d01-850b-1f08149ee930.png"></img>
<img src="https://user-images.githubusercontent.com/64320373/133108427-a1c8652b-6ded-4546-9364-4f09e3e0f8f1.png"></img>
<img src="https://user-images.githubusercontent.com/64320373/133108430-01f5f011-471c-4810-93c1-ff3363365e6b.png"></img>

## 7. 플렛 브레드 사의 광고 적용
https://www.gomcorp.com/service/video.gom, VAST 3.0 규격의 XML Parsing, TikXML 라이브러리 사용

## 8. WebView에서 History back 기능 구현

## 9. 기타 버그 수정
