# - 2024 전산통계학과&amp;데이터사이언스학과 9월 연광제 인생네컷

2024 9월 자연과학대학 축제인 연광제를 맞이하여 학과에서 인생네컷 프로그래밍을 해보았다. 

![image](https://github.com/user-attachments/assets/f2de6b07-1eca-4ba0-b7b5-1f4d9f655418)

이 이미지와 함께 인생네컷이 시작된다

카메라 혀용을 누르고 얼굴을 확인한 후 start버튼을 누르면 촬영이 시작된

![image](https://github.com/user-attachments/assets/1533c996-b68e-4f7a-9529-35ece981134f)

![image](https://github.com/user-attachments/assets/f14588aa-ff7e-42f8-a2ba-1bfb08fdadcc)

카메라 같은 경우는 camostudio라는 어플을 이용했는데 성능이 좋지않은 노트북 카메라를 아이패드나 스마트폰에 카메라로 연결해주는 어플이였다
이 프로그램을 돌릴때도 camostudio를 사용하여 내가 갖고있는 아이패드프로11인치 4세대를 이용하여 사진을 촬영했다.

![image](https://github.com/user-attachments/assets/943f7dbb-32cd-4fcc-8aa6-28977acbe09e)

![image](https://github.com/user-attachments/assets/59f79a8b-6bcb-448c-aaf4-ad6bf0f84f28)

촬영이 다 끝나면 이렇게 프레임을 고르는 장면이 나오게된다.

그 후에는 

![image](https://github.com/user-attachments/assets/18cf0b65-6dd9-4fcf-87a5-5bd0ad6a16b0)

이건 QR코드 만드는 버튼을 눌렀을때 로딩이 나오는 부분인데 이 로딩부분은 퍼온거지만 디자인이 이뻐서 나도 이런걸 나중에 만들어 보고싶어서 캡쳐해보았다. 

결론적으로 이제 QR코드가 나오고 인생네컷이 마무리된다.



마무리하면서
처음에 시작할때 어떤식으로 하면 좋을까 생각을 하다가 작년에는 어떻게 만들었는지 물어보았다. 허나 기억하는 사람이 별로없고 아이패드자체로 인생네컷이 진행되었다고해서 그럼 앱으로 만들어야되나? 하며 플러터라는 언어를 공부해보았지만 아이패드에서 앱이 구현되도록 하려면 맥이 필요하다하여서 결국 어플로 만드는건 포기를 하게되었다. 하지만 나에겐 아직 챗지피티가 남아있었고 html같은경우 자신있는 분야였기 떄문에 그래 html을 이용한 홈페이지를 만들어보자. 그리고 실제 인생네컷처럼 컴퓨터와 카메라가 연결되어서 사진을 찍는 형태가 구현되기만 한다면 충분히 좋은 퀄리티로 제약없는 인생네컷을 만들 수 있을것이라고 생각하였다.
인생네컷에서 가장 먼저 구현해야할것이 무엇일까 어떤게 구현이 성공적이어야 큰 틀에서 볼떄 중요할까 언어를 바꾸지 않아도 될까 라는 생각을 하였고 우선순위를 생각하고있었지만 인생네컷에는 모든 기능들이 중요하다는 결론이 나왔다. 노트북카메라가아닌 아이패드나 스마트폰 카메라연결, 사진 찍은걸 저장하고 프레임에 맞게 배치하는것, 배치가 잘되었고 프레임이 잘 적용되었다면 딱 프레임부분만 자른 후 그것을 사용자들에 핸드폰에 저장할 수 있게하는 기능 등 모든 기능들이 쇠사슬처럼 연결되어 하나의 큰 뭉텅이가 되었다. 만약 여기서 하나라도 html로 구현이 불가능하다면 지금까지 만든게 무용지물이 되기때문에 앞길이 막막하였다.

지피티에 도움을 받아 맨처음에 시작한건 사진을 찍고 내가 고른 프레임이미지 공간에 사진들을 위치에 맞게 배치하는 일을 먼저 작업하였다. 왜냐면 그게 인생네컷에서 가장 중요한 부분이고 구현해야할 제일 중요한 파트라고 생각하였기 때문이다. html에 canvas라는 태그를 사용하여 만들었는데 이 캔버스가 그림을 그리듯 사이즈가 있으면 그 위에 올려놓는게 가능하였다. 그리하여 노트북 캠을 이용하여 사진을 찍고 프레임위에 사진을 올려놓는걸 먼저했다. base64 인코딩이라는걸 이용해서 프레임을 가져오고 완성을 했다.

그 다음은 노트북과 아이패드 카메라를 연결하여 아이패드에 카메라가 노트북에 보이도록 하는 것이였다. 이것또한 지피티가 많은 어플을 알려주어 쉽고 빠르고 와이파이 없이 연결가능한 camostudio를 이용하여 찾고 해결하였다.

중간중간에 디자인이라든가. html구조등을 어떻게 할지 고민이 있었지만 여러 html파일을 만들기보단 block과 none을 이용하여 하나의 html파일이지만 여러개의 파일처럼 보이도록 만들었다. 여러 페이지를 사용하면 페이지간 이동할때 사진 전달이라거나 중간중간 끊기는 느낌이 들어서 이 기분을 들게 하고 싶지않았다. 이러한 방법의 문제점은 내가 지금 만드려는 구조를 머리속으로 생각하고 순서를 지정해줘야 한다는 거다 페이지를 여러개만들면 이 페이지는 이럴때 저건 저럴때 하면 되지만 하나의 페이지로 하고 모든것이 동시에 존재하니까 언제는 누가block이고 그때 이건none이어야하고 이런 복잡성이 있었지만 아이패드로 하나하나 구조를 잡아가면서 만들어보았다.

인생네컷에 마지막부분인 사진을 찍고 프레임을 완성시킨 다음에 어떻게 사용자에게 이 사진을 줄 것인가 이게 큰 문제점이였는데 지금까지 만든걸 전부 뒤집힐만큼 어떻게 할 방법이 없었다. 가장 기본적으로 qr코드를 이용해보았는데 qr코드는 무슨 cols였나 어떤 법칙에 위반되어서 anonymous이런걸 이용하라고 하였지만 이러한 개념을 잘 몰라서 힘들었다. 어떻게 하면 qr을 이용하고 오류가 뜨지 않을 수 있을것인가.. 
다양한 api를 이용하여 base64인코딩을 이용한 이미지를 가지고 큐알을 완성시켜보았다. 

마지막으로 제일 문제는 base64를 이용한 이미지의 화질문제와 인생네컷 프레임을 보면 사진보다 위에 입혀져있는 사진들이 존재하였고 이러한 사진들을 어떻게 처리해야할것인가였다.
뒤예꺼먼저 말하자면 인생네컷에 사진이 만들어지는 구조가 베이스가되는 프레임이미지를 아래깔고 그 위에 사용자가 찍은 사진을 위치에 맞게 네개를 배치하는 것이다. 그리하여 위로 이불덮어지듯 아래이미지는 보이지 않겓되는데 그럼 사진 위에 이미지는 어떻게 올려두어야 사진도보이고 프레임에 이미지도 들어갈 것인가 고민을 해보다가 아 누끼를 따면 되겠구나 사진에 배경을 지우거나 캐릭터들만 남기고 나머지를 다 지우면 되겠다 생각하여 베이스가 된 프레임 사진 -> 사용자 사진 -> 프레임 캐릭터 누끼딴 사진 이런 순서로 구현하여 성공하였다.

이제 모든건 완성이 되었지만 화질이 제일 문제였다. 확대를 하면 깨지는건 당연하였고 확대를 안해도 화질이 영 좋지는 않았다. 화질문제같은경우는 일단 base64를 이용한게 컸다고 생각한다. 그래서 따로 서버를 만들고 이미지를 거기 올리고 받아오는 느낌을 하고싶었지만 그렇게하니 아까 말한것처럼 어떤 법치에 위배되어서 큐알 코드가 나오지 않았다. 일단은 사진의 화질을 좋게만들어보았고 프레임은 하지 못하였지만 또 나에게는 챗지피티가 있었고 imgbb나 imgur의 이미지를 올리는 기술을 사용하여 서버상에 이미지를 올리고 이미지 주소를 이용하여 큐알코드가 잘 구동되도록하였다. 또한 누끼도 화질이 좋지않았는데 remove.bg라는 홈페이지에서 하다가 미리캔버스에 배경제거하기 기술을 이용하여 누끼땐 화질도 좋아지게 만들어서 결론적으론 꽤 만족하는 결과물을 얻게 되었다. 여기서 더 좋은 화질을 원하는건 돈을 지불하여야 했기때문에 현재에 나로써는 여기까지만 하는게 가장좋다고 판단하였다.

프로그램을 만들다보면 이 폴더와 코드들에게 많은 정이 들어가는 것 같다. 이제 연광제가 끝나고 나의 삶으로 돌아와서 작성하는것이지만 다시는 이 프로그램을 사용하지 않을것이고 이 폴더를 지나칠 것에 애인이랑 이별한 것과 같이 마음이 너무 아프다.

긴 글을 쓰게해줘서 고맙고 많은 추억이 담겨져있는 힘들었던 시기에 만들어져 나의 마음이 담겨져있는 인생네컷을 마무리하겠다.







