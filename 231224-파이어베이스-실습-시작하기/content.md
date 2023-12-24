# 파이어베이스 프로젝트 만들기

Firebase 홈페이지에 들어간 뒤 <span style="color:orange">**프로젝트 만들기**</span> 버튼을 누른다.
![파이어베이스 홈페이지](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EB%A7%8C%EB%93%A4%EA%B8%B0.png?raw=true)  
첫번째 페이지에서 프로젝트 이름은 FirebaseStart,  
두번째 페이지에서 애널리틱스 사용하기 체크,  
세번째 페이지에서 Default Account for Firebase 선택 후 생성하였다.  
</b>
생성을 완료하면 아래와 같은 화면이 뜰것이다.
![파이어베이스 로그인 성공](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%83%9D%EC%84%B1%EC%99%84%EB%A3%8C.png?raw=true)
여기서 가운데 보이는 Unity 로고를 클릭하면 유니티용 파이어베이스 앱을 세팅할 수 있는데,  
바로 하지 말고 유니티에서 앱id를 미리 확인해주는 것이 좋다.  
</b>  
유니티 프로젝트를 열고 Edit->Project Settings의 Player 탭에 들어가면 아래와 같이 Company Name과 Product Name을 수정할 수 있다.  
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/%EC%9C%A0%EB%8B%88%ED%8B%B0%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%84%A4%EC%A0%95.png?raw=true)  
여기서 원하는 이름을 지어주면 된다.  
나는 Company Name을 "FirebaseWithUnity"로, Product Name을 "FirebaseStart"로 지었다.  
그리고 밑의 Other Settings 탭을 열어서 아래로 쭉 내렸을 때 <u>Mac App Store Options</u>에 있는 Override Default Bundle Identifier 토글을 한번 껐다 키고, Bundle Identifier의 문자열을 복사해서 Android 앱 등록에 사용한다.
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/%EC%9C%A0%EB%8B%88%ED%8B%B0%EC%95%B1id%EB%B3%B5%EC%82%AC.png?raw=true)
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/android%EC%95%B1%EB%93%B1%EB%A1%9D.png?raw=true)  
그 다음 단계에서는 google-services.json 파일을 다운받으라고 한다.  
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/googleservices.png?raw=true)  
다운받고 나면 유니티 프로젝트 폴더에서 Assets->StreamingAssets 폴더 하위에 드래그해주면 된다.  
만약에 StreamingAssets 폴더가 없으면 같은 이름의 폴더를 하나 생성하고 난 뒤 넣어주자.
![]()

그 다음 SDK 압축파일을 다운로드 하라고 뜨는데, 다운받고 압축을 푼다. 용량이 1GB쯤 되니 시간이 좀 걸린다.  
다운받고 압축을 풀면 폴더가 하나 나오는데, 이 안에 기능별로 .unitypackage 파일들이 들어있다.  
필요한 기능을 사용할 때마다 이 unitypackage 파일을 실행해서 라이브러리 파일들을 설치하면 된다.

만약에 유니티 에디터 설치할 때 IOS sdk를 설치하지 않았으면 유니티 콘솔창에 에러가 뜰 텐데, 이건 Firebase sdk에서 기본적으로 IOS 라이브러리에 접근하려고 하기 때문에 뜨는 오류이다. 무시해도 실행은 되지만 에러메세지 보기 싫으니 지우자.

오류 메세지를 클릭하면 문제가 있는 에셋파일이 뜨는데, 각각 인스펙터에서 Define Constraints 옵션에다가 +버튼을 누른 뒤 UNITY_IOS 문자열을 넣어주면 된다. 입력하면 유니티가 컴파일을 다시 해야하니, 오른쪽 아래의 progress bar가 사라질때까지 기다리자.
