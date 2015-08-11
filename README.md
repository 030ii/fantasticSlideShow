# fantasticSlideShow
프로젝트 : 배경 이미지 슬라이더 라이브러리를 만들자!

설명 (프로젝트 동기 및 설명) : 
이미지 슬라이더 관련 라이브러리는 세상에 수없이 많이 있습니다.
그런데 막상 개발을 하다가 이미지 슬라이드를 넣고 싶을 때 검색을 해보면, 
너무 많아서/남의 코드라 복잡해서/내가 원하는 부분만 딱 가지고 오기가 어려워서 등의 이유로
결국 직접 하드코딩으로 만들곤 합니다.
세상에 널리고 널린 이쁜 라이브러리를 내맘대로 못쓰고 있는 그대로만 써야하는 것이 불편했습니다.
앞으로는 내가 원하는 효과와 슬라이드 방식으로 언제든 사용할 수 있도록
나만의 이미지 슬라이드 라이브러리를 만들고 싶습니다.

이번 프로젝트에서는 기본적인 장면 전환 효과(서서히 밝아지기, 좌우 슬라이드, 상하 슬라이드)을 구현할 것이고, 
(그밖에 여러가지 이쁜 장면방식들은 이 프로젝트가 완료되면 손쉽게 추가할 수 있을 것 같으니, 그건 나중에 개발하고 일단은 기본 장면 전환 방식 3가지만 다루겠습니다.)
슬라이드하는 방법은 자동으로 전환, 이전/다음 버튼 클릭 시 전환, 동그라미(혹은 번호) 버튼 클릭 시 전환 하는 방식 모두 적용할 계획입니다.
그리고 사진에는 필터가 적용되어 사진에 마우스 오버로 필터가 on/off될 수 있도록 할 계획입니다.

앞에 말한 효과와 방법이 모두 구현 완료가 되면 이것을 라이브러리화 시켜서
사용자가 직접 전환 효과를 선택해서 이 라이브러리를 사용할 수 있도록 연동(?)할 계획입니다.



- 사용자는 사용할 배경이미지들을 img폴더를 만들어 bg1.jpg , bg2.jpg, ... 로 직접 지정해야한다.
     //    img / 
     //       bg0.jpg
     //       bg1.jpg

- 라이브러리 사용하기 위한 코드를 추가한다.
    container.slideBg(사진 개수, 슬라이드 효과);
    ex) container.slideBg(5, fadeIn)


    // container {
    //     find bg_box
    // }
    // container.slideBg(5,leftS)



- 라이브러리 설명 
효과는 현재 3가지(가장 기본적인 장면효과)     // 나중에 시간이 남거나 프로젝트가 끝난 이후에 재미있는 효과를 추가할 생각
    슬라이드 효과1 = 서서히 밝게(fadeIn)
    슬라이드 효과2 = 좌우로 슬라이드(horizontal)
    슬라이드 효과3 = 상하로 슬라이드(vertical)

    슬라이드 방법1 = 자동 전환
    슬라이드 방법2 = 이전/다음 화살표 클릭 시 전환
    슬라이드 방법3 = 동그라미(혹은 번호 버튼) 클릭 시 전환


    개발 방법 고민사항 - 슬라이드 효과는 css로 짤지, js로 짤지.... 코딩 자체는 css가 쉽고 짧긴 함.
                    (그런데 js라이브러리니까 js로 짜야하지 않을까?)


filter, css animation

- 개발 계획
    week1 (css animation)
        - html/css 구조 잡기(이전/다음 화살표도 만들기)    
        - 효과1 구현(방법1로 구현) 
    week2 (css animation)
        - 방법2(이전/다음 화살표 클릭 시 전환) 구현
        - 효과2, 효과3 구현(방법1로 구현)
    week3 
        - 사진 개수에 따라 동그라미 버튼 display
        - 방법3(동그라미 클릭 시 전환) 구현
    week4 (filter)
        - 마우스 오버시 필터 on/off될 수 있도록 한다.
        - 구현 완료된 3가지 효과 중 하나를 사용자가 선택해서 슬라이드 쇼 할 수 있도록 구현
        - 모듈화 
    week5 
        - 코드 개선
        - 라이브러리 등록
        - 시간 남으면 장면 효과 추가




    참고 사이트 :
http://www.jssor.com/index.html  -- 여러가지 슬라이드 쇼 모음 사이트
www.10x10.co.kr — 효과 2, 방법1-2 다 있음
www.tumblr.com — 효과3
http://tympanus.net/Tutorials/FullscreenSlitSlider/index2.html -- 이쁨
