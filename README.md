# 감귤마켓 : **멋쟁이사자처럼 프론트엔드 1기** 팀 프로젝트

**SNS 클론코딩** : [감귤마켓](http://146.56.183.55:3000/)       
팀원 : 장효순, 강지승, 한진실, 주현호    

## 개요
감귤마켓 프로젝트는 **SNS를 직접 구현한 프로젝트**입니다.    
**게시글에 대한 CRUD와 회원가입, 로그인 기능**을 제공합니다.     


## 기능 및 디자인 참조 링크
1. 기능 : [요구사항 명세서](https://paullabworkspace.notion.site/SNS-cdd5ed88a24b499593d7081dc28a5cbc#85eb0582eafa45939c0f7d0f67b02fbb)
2. 디자인 : [피그마 링크](https://www.figma.com/file/Gn6gQJdYwImYsEYSzBXhud/%EB%A9%8B%EC%82%AC_%ED%94%84%EB%A1%A0%ED%8A%B8%EC%97%94%EB%93%9C%EC%8A%A4%EC%BF%A8?node-id=39%3A1814)

## 개발 환경
**OS** : Mac, Window    
**Frontend**: HTML, CSS, JavaScript    
**Backend** : [API 명세](https://paullabworkspace.notion.site/API-b9c93280e29f4670b324009d4461f4d5) [서버 API](http://146.56.183.55:5050/) # 해당 서버가 닫혀있을 시 프로젝트가 제대로 동작하지 않을 수 있음.        
**IDE** : VS Code   
**Team Collaboration Tool** : Git, Git Projects, Discord       
**Platform** : Mobile Web        
**Test Browser** : Chrome Version 97.0.4692.71, Safari Version 15.2      
**Test Device** : iPhoneSE/XR, Gallaxy S12       

## 기능 구현 상세
<table style="width: 100%;">
    <thead>
      <tr>
        <th colspan="3" style="background:black;color:white;text-align:center;">감귤마켓 SNS 팀 프로젝트 진행 현황</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>이름</th>
        <th>주요 기능</th>
        <th>참조 번호</th>
      </tr>
      <tr>
        <td>장효순</td>
        <td>
            로그인, 회원가입, 프로필 수정, 홈 피드 디자인 및 기능 구현
        </td>
        <td>
            1~4, 8
        </td>
      </tr>
      <tr>
        <td>강지승</td>
        <td>
            프로필 피드, 팔로잉/팔로워 디자인 및 기능 구현
        </td>
        <td>
          5~7
        </td>
      </tr>
      <tr>
        <td>한진실</td>
        <td>
          상품,게시글,댓글 등록/수정/삭제, 채팅목록 디자인 및 기능 구현
        </td>
        <td>
          9~12
        </td>
      </tr>
      <tr>
        <td>주현호</td>
        <td>
          채팅방, 하단 탭 메뉴, 좋아요 버튼, 모달창 디자인 및 기능 구현
        </td>
        <td>
          13~16
        </td>
      </tr>
    </tbody>
  </table>

✅ 체크리스트✅         
**1. splash**☑️
- 서비스 접속 초기화면
- splash 화면이 잠시 나온 뒤 다음 페이지가 나타납니다.
    - 로그인을 하지 않은 경우 : 로그인 화면
    - 로그인이 되어 있는 경우 : 감귤마켓 피드☑️

**2. 로그인**☑️

- 로그인은 **로그인 메인 화면**과 **이메일 로그인 화면**으로 나눠져 있습니다.
- SNS(카카오톡, 구글, 페이스북) 로그인은 구현하지 않으며, 화면에 버튼만 배치☑️
- 로그인 메인 화면에서 `이메일로 로그인` 을 클릭하면 이메일로 로그인할 수 있는 화면으로 이동
- 이메일과 비밀번호를 모두 입력하면 `다음` 버튼이 활성화 됩니다. 입력되지 않은 입력창이 있다면 버튼은 활성되지 않습니다.
- `로그인` 버튼을 클릭하면 이메일 주소와 로그인에 대한 유효성 검사를 진행하며, 이메일 주소 또는 비밀번호가 일치하지 않을 경우에는 경고 문구가 나타납니다.
- 입력창에 focus 될 경우에는 선의 색이 변합니다.(회색, #DBDBDB → 주황색, #F26E22)

**3. 회원가입**☑️

- 로그인 메인 화면에서 `회원가입` 을 누르거나 이메일 로그인 화면에서 `이메일로 회원가입` 을 누르면 회원가입 화면이 나타납니다.
- 회원가입 페이지에서는 유효성 검사가 로그인 페이지와 조금 다르게 진행됩니다.
- 이메일 주소 또는 비밀번호를 입력하고 입력창에서 포커스를 잃으면 바로 유효성 검사가 진행되고 통과하지 못한 경우 경고 문구가 각 입력창 하단에 표시됩니다.
- 이메일 주소의 형식이 유효하지 않거나 이미 가입된 이메일일 경우,  또는 비밀번호가 6자 미만일 경우에는 각 입력창 하단에 경구 문구가 나타납니다.
- 입력창에 focus 될 경우에는 선의 색이 변합니다.(회색, #DBDBDB → 주황색, #F26E22)
- 작성이 완료된 후, 유효성 검사를 통과할 경우 `다음` 버튼이 활성화되며, 버튼을 클릭하면 프로필 설정 폼이 나타납니다.
- 프로필 설정에 필요한 프로필 사진, 사용자 이름(2~10자 이내), 계정 ID, 소개를 입력받습니다.
    - 프로필 사진은 등록하지 않을 경우 기본 이미지가 등록되게 합니다.
    - 사용자 이름과 소개는 다른 사용자와 중복될 수 있습니다.
    - 계정 ID는 중복이 불가합니다.
    - 프로필 설정에서도 같은 방식으로 유효성 검사가 진행됩니다. 계정 ID에 대한 중복 유무와 형식을 검사합니다.

**4. 감귤마켓 피드(홈 화면)**☑️

- 감귤마켓 피드는 사용자들이 올린 게시글들이 표시되는 페이지
- 감귤마켓 피드에는 자신이 팔로우한 사용자의 게시글만 확인할 수 있습니다.
- 팔로우한 사용자가 없을 경우와 내가 팔로우한 사용자가 올린 게시글이 없는 경우 "유저를 검색해 팔로우 해보세요!" 문구와 함께 `검색하기` 버튼이 표시됩니다.☑️

**5. 검색**☑️

- 감귤마켓 피드 상단에 돋보기 버튼(검색 버튼)을 클릭하면 표시되는 페이지입니다.
- 사용자 이름을 검색할 수 있는 페이지입니다.
- 필수 과제에서는 검색 기능은 구현하지 않습니다. 마크업만 구현해 보세요.☑️

**6. 사용자 프로필 페이지**☑️

- 사용자 프로필 페이지에서는 사용자 이름, 계정 ID, 소개, 팔로워 및 팔로잉 수, 판매 상품, 그리고 사용자가 업로드한 게시글을 확인할 수 있습니다.
- 사용자 정보 하단에는 팔로우 버튼이 있습니다. 팔로우 버튼을 클릭하면 언팔로우 버튼으로 바뀌어야 합니다. 단, 팔로우 기능은 구현하지 않습니다. 버튼의 변화만 구현하세요.☑️
- 팔로워 및 팔로잉 수를 클릭하면 팔로워, 팔로잉 사용자 목록이 표시됩니다.
- 판매 중인 상품 섹션은 등록한 상품이 없을 경우에는 표시되지 않습니다.
- 게시글 섹션에서는 목록형과 앨범형으로 게시글들을 확인할 수 있습니다. 기본형은 목록형이며, 이미지가 없는 게시글을 경우에는 앨범형에서는 표시되지 않습니다.
- 또한 사용자가 올린 게시글이 없을 경우에는 게시글이 나타나지 않습니다.
- 나의 프로필 페이지일 경우
    - 프로필 수정 버튼과 상품 등록 버튼이 표시됩니다.
    - 판매 중인 상품을 클릭하면 하단에 상품 삭제, 수정, 웹사이트에서 상품 보기 버튼이 포함된 메뉴가 나타납니다. (단, 나의 프로필 페이지가 아닐 경우 상품을 클릭하면 바로 상품 판매 사이트로 이동됩니다.)☑

**7. 팔로워, 팔로잉 목록**☑️

- 사용자 프로필 페이지에서 팔로워 및 팔로잉 수를 클릭하면 나타나는 페이지
- 목록은 사용자 프로필 사진, 이름, 계정 ID, 팔로우(또는 취소) 버튼으로 구성됩니다.
- 내가 팔로우 한 사용자일 경우 취소 버튼이, 내가 팔로우 하지 않은 사용자일 경우에는 팔로우 버튼이 표시됩니다. 단, 팔로우 기능은 구현하지 않습니다. 버튼의 변화만 구현하세요.☑️

**8. 내 프로필 수정**☑️

- 나의 프로필 페이지에서 `프로필 수정` 버튼을 클릭하면 프로필을 수정할 수 있는 페이지가 나타납니다.
- 입력창에 대한 명세는 회원가입에서의 프로필 설정과 동일합니다. 유효성 검사가 통과되지 않을 경우 `저장` 버튼이 활성화되지 않습니다.☑️

**9. 상품 등록**☑️

- 나의 프로필 페이지에서 `상품 등록` 버튼을 클릭하면 상품을 등록할 수 있는 페이지가 나타납니다.
- 상품 이미지, 상품명, 가격, 판매링크를 입력받을 수 있으며, 모든 입력이 완료되면 `저장` 버튼이 활성화됩니다.
- 상품명은 2~15자 이내로 입력되게 하고, 가격은 숫자를 입력하면 자동으로 원단위로 변환시킵니다.☑️

**10. 게시글 댓글 페이지**☑️

- 게시글 하단에 말풍선 아이콘을 클릭하면 댓글을 확인하고 입력할 수 있는 페이지가 나타납니다.
- 댓글 입력창에 텍스트를 입력하면 `게시` 버튼이 활성화됩니다.

**11. 게시글 작성 페이지**☑️

- 게시글을 작성할 수 있는 페이지로, 하단 메뉴바에서 `게시글 작성` 을 클릭하면 표시됩니다.
- 글이 입력되거나 사진이 업로드 되면 `업로드` 버튼이 활성화되고, 버튼을 누르면 게시글이 업로드됩니다.
- 사진은 우측 하단 버튼을 클릭하면 업로드할 수 있으며, 최대 3장까지 업로드 가능합니다.

**12. 채팅 목록**☑️

- 채팅 목록과 채팅방은 마크업 구현 및 스타일 적용만 진행합니다.☑️
- 현재 대화가 진행 중인 채팅 목록이 표시됩니다.
- 내가 읽지 않은 메시지가 있는 채팅방인 경우 프로필 사진 좌측 상단에 작은 원으로 표시됩니다.☑️

**13. 채팅방**☑️

- 채팅 목록과 채팅방은 마크업 구현 및 스타일 적용만 진행합니다.☑️
- 채팅 목록에서 목록 아이템을 클릭하면 해당 채팅방이 나타납니다.
- 채팅 기능은 구현하지 않습니다.☑️
- 채팅 입력창에서 텍스트가 입력되면 `전송` 버튼이 활성화됩니다.☑️
- 이미지 버튼을 클릭하고 이미지를 선택하면 전송 버튼이 활성화됩니다.
- 채팅방 상단 우측 버튼을 클릭하면 아래와 같은 모달이 화면 하단에 나타납니다.

**14. 하단 탭 메뉴**☑️

- 하단 탭 메뉴는 홈, 채팅, 게시물 작성, 프로필 4개의 메뉴로 구성되어 있습니다.
- 모든 페이지는 페이지 경로에 해당하는 탭 메뉴가 활성화됩니다.

**15. 좋아요 버튼**☑️

- 게시글이 나타나는 모든 페이지에 해당합니다.
- 게시글 하단에는 하트 모양에 좋아요 버튼이 있습니다.
- 빈 하트를 클릭하면 색이 칠해진 하트로 변하고, 색이 칠해진 하트를 누르면 빈 하트로 변합니다.
- 좋아요 기능은 구현하지 않습니다.

**16. 모달 버튼**☑️

- 우측 버튼을 클릭하면 아래와 같은 모달이 화면 하단에 나타납니다.
    
- 헤더에 있는 버튼을 클릭하면 설정 및 개인정보와 로그아웃이 나타납니다.
- 게시글 우측 상단에 위치한 버튼을 클릭했을 경우
    - 내가 작성한 게시글일 경우 : 삭제, 수정 버튼이 나타납니다.
    - 다른 사용자가 작성한 게시글일 경우 : 신고하기 버튼이 나타납니다.

- 댓글 우측 상단에 위치한 버튼을 클릭했을 경우
    - 내가 작성한 댓글일 경우 : 삭제 버튼이 나타납니다.
    - 다른 사용자가 작성한 댓글일 경우 : 신고하기 버튼이 나타납니다.
- 로그아웃, 삭제, 신고 버튼을 누르면 확인 메시지 모달창이 나타나야 하고, 취소 버튼을 누르면 모달은 사라집니다.

## 기타 도전 기능
**팔로우**☑️
- 사용자 정보 하단에는 팔로우 버튼이 있습니다. 내가 팔로우 한 사용자일 경우 언팔로우 버튼이, 내가 팔로우 하지 않은 사용자일 경우에는 팔로우 버튼이 표시됩니다.
- 팔로우 목록에는 내가 팔로우 한 사용자일 경우 취소 버튼이, 내가 팔로우 하지 않은 사용자일 경우에는 팔로우 버튼이 표시됩니다.
- 팔로우 버튼을 클릭하면 팔로잉 목록에 해당 사용자가 추가됩니다. 취소 버튼을 클릭하면 팔로잉 목록에서 해당 사용자가 삭제되어야 합니다.
- 사용자 프로필 페이지에서 팔로워 및 팔로잉 수를 클릭하면 나타나는 페이지입니다.
- 팔로워 및 팔로잉 목록에 내가 표시될 경우 팔로우 버튼은 나타나지 않습니다.☑️

**좋아요**☑️
- 게시글이 나타나는 모든 페이지에 해당합니다.
- 게시글 하단에는 하트 모양에 좋아요 버튼이 있습니다.
- 빈 하트를 클릭하면 색이 칠해진 하트로 변하고, 색이 칠해진 하트를 누르면 빈 하트로 변합니다.
- 좋아요 개수는 카운트 되어 하트모양 우측에 표시됩니다.

**댓글**☑️
- 댓글 삭제 및 신고하기 기능을 구현합니다.☑️
- 댓글 작성이 현재 시간으로 부터 몇 초, 분, 시간 전에 작성되었는지 표시합니다.☑️
- 댓글 개수는 카운트 되어 말풍선 아이콘 우측에 표시됩니다.☑️

**검색**☑️
- 감귤마켓 피드 상단에 돋보기 버튼(검색 버튼)을 클릭하면 표시되는 페이지입니다.
- 사용자 이름과 계정을 검색할 수 있는 페이지입니다. 입력창에 텍스트를 입력하면 해당하는 사용자가 나오도록 합니다.☑️
- 검색어와 같은 단어에는 주황색 글씨가 표시됩니다.☑️

## 향후 계획
**Refactorying**
- 중복코드 모듈화
- 파일 통합

**Backend**
- 서버 구축
- 배포


## Directory 구성 (HTML, CSS, JS)
```
.
├── README.md
├── images
│   ├── 중략
│   └── ...
├── pages
│   ├── 1.splash.html
│   ├── 2.login.html
│   ├── 2.login_email.html
│   ├── 3.join_email.html
│   ├── 4.home.html
│   ├── 5.search.html
│   ├── 6.profile.html
│   ├── 7.followers.html
│   ├── 8.profile_modification.html
│   ├── 9.addProduct.html
│   ├── 11.uploadPage.html
│   ├── 12.chat_list.html
│   ├── 13.chat_room.html
│   ├── 15.like_button.html
│   ├── 16.modal.html
│   ├── index.html
│   ├── module.html
│   ├── page-404.html
│   └── test_modal.html
├── css
│   ├── 1.login.css
│   ├── 2.signin.css
│   ├── 3.join_membership.css
│   ├── 4.home.css
│   ├── 5.search.css
│   ├── 6.profile.css
│   ├── 7.followers.css
│   ├── 8.profile_modification.css
│   ├── 9.addProduct.css
│   ├── 11.uploadPage.css
│   ├── 12.chat_list.css
│   ├── 13.chat_room.css
│   ├── 15.like_button.css
│   ├── modal.css
│   ├── module.css
│   ├── page-404.css
│   └── reset.css
└── scripts
    ├── 1.splash.js
    ├── 2.login.js
    ├── 3.join.js
    ├── 4.home.js
    ├── 5. search.js
    ├── 6. profile.js
    ├── 7. followers.js
    ├── 9.addProduct.js
    ├── 11.uploadPage.js
    ├── 15.like_button.js
    ├── modal.js
    ├── script.js
    └── test_modal.js
```

## License
감귤마켓 SNS는 **멋쟁이 사자처럼 프론트엔드 1기 과정에서 진행된 프로젝트**이며 사용된 **이미지, 서버 API**는 **(주)위니브**로부터 제공받았습니다.     

페이지별 UI/UX 디자인 레퍼런스는 [피그마](https://www.figma.com/file/Gn6gQJdYwImYsEYSzBXhud/%EB%A9%8B%EC%82%AC_%ED%94%84%EB%A1%A0%ED%8A%B8%EC%97%94%EB%93%9C%EC%8A%A4%EC%BF%A8?node-id=39%3A1814)를 활용했으며,     
**일부 서버 API 요청 코드를 제외**한 **모든 HTML/CSS/JavaScript 코드**는 팀원들이 직접 작성하였습니다.
