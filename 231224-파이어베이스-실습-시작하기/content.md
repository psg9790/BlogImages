# 파이어베이스 프로젝트 만들기

Firebase 홈페이지에 들어간 뒤 <span style="color:orange">**프로젝트 만들기**</span> 버튼을 누른다.
![파이어베이스 홈페이지](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EB%A7%8C%EB%93%A4%EA%B8%B0.png?raw=true)  
나는 프로젝트 이름을 "FirebaseStart"로 하고, 애널리틱스 사용하기, Default Account for Firebase를 선택하고 생성하였다.  
프로젝트 생성이 완료되면 앱을 만들 수 있는데, 바로 하지 말고 유니티에서 선행작업을 먼저 해주는 것이 좋다.

## 유니티 bundle id 설정

유니티 프로젝트를 열고 Edit->Project Settings의 Player 탭에 들어가면 아래와 같이 Company Name과 Product Name을 수정할 수 있다.  
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/%EC%9C%A0%EB%8B%88%ED%8B%B0%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%84%A4%EC%A0%95.png?raw=true)  
여기서 원하는 이름을 지어주면 된다.  
나는 Company Name을 "FirebaseWithUnity"로, Product Name을 "FirebaseStart"로 지었다.  
그리고 밑의 Other Settings 탭을 열어서 아래로 쭉 내렸을 때 <u>Mac App Store Options</u>에 있는 Override Default Bundle Identifier 토글을 한번 껐다 키고, Bundle Identifier의 문자열을 복사해서 Android 앱 등록에 사용한다.  
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/%EC%9C%A0%EB%8B%88%ED%8B%B0%EC%95%B1id%EB%B3%B5%EC%82%AC.png?raw=true)

## 파이어베이스 유니티용 앱 생성

위에서 파이어베이스 프로젝트를 생성하고 나면 아래와 같은 화면을 볼 수 있을 것이다.
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%83%9D%EC%84%B1%EC%99%84%EB%A3%8C.png?raw=true)
여기서 가운데 보이는 Unity 로고를 클릭하면 유니티용 파이어베이스 앱을 세팅할 수 있다.  
본격적으로 파이어베이스에서 유니티용 프로젝트 만들기 버튼을 누르면, 첫번째 단계에서 패키지를 등록하는 창이 나온다.  
여기에 위에서 복사한 Bundle Identifier를 붙여넣고 진행해주면 된다.  
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/android%EC%95%B1%EB%93%B1%EB%A1%9D.png?raw=true)  
그 다음 단계에서는 google-services.json 파일을 다운받으라고 한다.  
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/googleservices.png?raw=true)  
다운받고 나면 유니티 프로젝트 폴더에서 Assets->StreamingAssets 폴더 하위에 드래그해주면 된다.  
만약에 StreamingAssets 폴더가 없으면 같은 이름의 폴더를 하나 생성하고 난 뒤 넣어주자.
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/streamingservices.png?raw=true)

그 다음 SDK 압축파일을 다운로드 하라고 뜨는데, 다운받고 압축을 푼다.  
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/sdk%EB%8B%A4%EC%9A%B4%EB%A1%9C%EB%93%9C.png?raw=true)  
용량이 1GB쯤 되니 시간이 좀 걸린다.  
다운받고 압축을 풀면 폴더가 하나 나오는데, 이 안에 기능별로 .unitypackage 파일들이 들어있다.  
새로운 기능이 필요할 때마다 이 패키지 파일을 실행해서 라이브러리를 설치하면 된다.  
![](https://github.com/psg9790/BlogImages/blob/main/231224-%ED%8C%8C%EC%9D%B4%EC%96%B4%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%8B%A4%EC%8A%B5-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0/packagesinproject.png?raw=true)  
나는 로그인 기능인 **FirebaseAuth**를 설치해보았다.

## IOS 에러

만약 유니티 IOS sdk를 설치하지 않았으면 유니티 콘솔창에 에러가 뜰 텐데, 이건 Firebase sdk에서 IOS용 코드에 접근하려고 하기 때문에 뜨는 오류이다.  
무시해도 실행은 되지만 에러메세지 보기 싫으니 지우자.  
console에서 오류메세지를 클릭하면 문제 파일이 프로젝트에 하이라이트 되는데, 그걸 클릭.  
각각 inspector창에서 Define Constraints 옵션에다가 +버튼을 누른 뒤 "UNITY_IOS"를 넣어주면 된다. 입력후 아래의 apply 버튼을 누르면 유니티가 다시 컴파일을 해야하니, 오른쪽 아래의 progress bar가 사라질때까지 기다려주자.

만약 오류 메세지를 눌렀을 때 하이라이팅이 안되면

-   ExternalDependencyManager->Editor->{1.2.177(version)}->Google.IOSResolver
-   Firebase->Editor->Firebase.Editor
    이 두개가 아마 오류 출처일 것이다. 이거 두개 수정하자.
