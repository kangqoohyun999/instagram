# 컬러 네임 (color name)

## RGB 또는 RGBA 코드 (Decimal)
<RGB>
선택자 {
    color : rgb(255, 255, 255);
}
<RGBA> - a는 투명도를 결정
선택자 {
    color : rgba(255,255,255,0~1);
}

## 16진수 컬러 코드 (Hex RGB)
선택자 {
    color : #FFFFFF;
}

# 글자를 표현하는 스타일
선택자 {
    color : #FFFFFF;
    font-style : italic;
    font-weight : 100;
    font-variant : small-caps;
    font-size : 15px;
    font-family : 폰트 이름;
    text-align : center;
    text-decoration " underline;
}

* color : 글자의 색상을 변경합니다. RGB 컬러 코드, 16진수 컬러 코드 등을 입력하여 적용한다.
* font-style : 주로 폰트를 기울임꼴로 표현하기 위해서 사용한다. 스타일 값은 italic, oblique(italic 오류 시 보조수단) 이다.
* font-weight : 글자의 두께를 의미한다. 100~900 사이의 숫자 입력 가능, 숫자가 클수록 글자가 두꺼워짐. <'strong'> 태그를 대체하는 용도이다.
* font-variant : 글꼴의 장평을 지정하는 등 여러 가능이 있지만, 주로 대소문자를 강제로 변환하는 용도로 사용된다. 대문자는 그대로 두고, 소문자는 크기가 작은 대문자 형태로 출력된다. <'h'> 태그와 함께 사용하면 멋진 제목 스타일을 연출할 수 있다.
* font-size : 폰트 크기를 지정하기 위한 용도로 사용된다. 스타일 속성값으로 픽셀 단위로 사이즈를 입력하면 된다.
* font-family : 글꼴을 변경하는 기능을 수행한다. VSCode에서 font-family까지 입력하고 콜론(:)을 찍을 때, 팝업으로 적용 가능한 항목들의 목록이 표시된다. 기본적으로 제공되는 폰트의 종류에는 한계가 있으므로, <'link'> 태그를 활용해 외부 폰트를 가져와 HTML에 부착시키고 이를 다시 CSS에서 불러와 사용하는 경우가 많다.
* text-align : 글자의 정렬 방향을 지정하는 스타일이다. 왼쪽 정렬, 오른쪽 정렬, 가운데 정렬을 지정할 수 있다. 하지만 text-align 속성은 글자보다는 그림이나 동영상 등 다른 정보를 정렬할 때 더 많이 사용된다.
* text-decoration : 글자에 밑줄을 그을 때 사용한다. 그런데, 줄을 문자의 아래에만 기재할 수 있는 것이 아니다. 밑줄을 삽입할 때는 underline, 윗줄을 삽입할 때는 overline, 취소선을 입력할 때는 line-through를 입력한다. 또한 색상도 지정할 수 있다.

# 공간을 표현하는 스타일
공간의 단위
1. %
부모 대비 비율이다. 예를 들어 CSS에서 넓이가 30%라는 이야기는, 부모 태그의 너비의 30%만큼의 공간을 의미한다.
2. auto
브라우저가 자동으로 계산하게 만드는 값이다. 단독으로 사용되는 경우는 흔하지 않다. 주로 margin과 padding 설정 시에 사용된다.
3. vw, vh
브라우저 창의 해상도를 기준으로 삼는 길이의 단위이다. 예를 들어, 100vw는 브라우저 화면 너비의 100%를 의미하며 30vw는 화면 너비의 30%를 의미합니다. vh도 마찬가지로, 100vh는 화면 높이의 100%를 의미한다. vw와 vh를 활용하면 화면의 크기에 상관없이 항상 일정한 비율로 화면에 콘텐츠를 표현할 수 있다. 특히 vh보다는 vw가 중요도가 높다.

# 크기 지정하기
일반적으로 크기를 지정할 때는 width 스타일 속성과 height 속성을 활용하면 좋다.
둘 중 하나의 값을 auto로 지정할 경우, 비율을 최대한 유지할 수 있도록 자동으로 계산되어 화면에 표시된다.
사실 auto값은 생략해도 정상적으로 작동한다.

# 영역을 표현하는 스타일
## 영역의 테두리를 표현하는 border
1. 선의 종류 - border
dotted, dashed, solid, double, inset, outset
2. 선의 두께 - border-width
3. 선의 색상 - border-color
4. 단축 표현
여러 종류의 색이나 선 종류를 섞어서 사용할 것이 아니라면 한 줄에 여러 속성 값을 입력하여 border를 설정할 수도 있다. 정보의 순서는 섞여도 상관이 없다.
ex.
#first{
    border: 5px red solid;
}
5. 둥근 모서리 - border-radius
border-radius 속성을 활용하여 border의 모서리를 둥글게 만들 수 있다. 속성값으로는 길이 단위를 입력할 수 있다. (픽셀, 퍼센트 둘다 가능)
#first{
    border: 5px red solid;
    border-radius: 5px;
}
정사각형 이미지에 50%를 입력하면 사진이 원형으로 잘린다.
img{
    width:200px;
    height:200px;
    border: 5px red solid;
    border-radius: 105px;
}
네 모서리의 곡률을 모두 다르게 주고 싶다면 각각의 모서리에 적용할 반지름을 하나씩 입력하면 된다. 좌측 상단 모서리부터 시계방향으로 곡률이 적용된다.

# 영역의 배경을 표현하는 background
1. 배경의 색상을 결정하는 background-color
background-color 스타일 속성을 활용하면 HTML 요소에 배경색을 입힐 수 있다.
p{
    background-color:yellow;
}
2. 배경에 이미지를 삽입하는 background-image
background-image 스타일 속성을 활용하면 요소의 배경에 이미지를 삽입할 수 있다. 스타일 값으로는 url()을 활용한다. 이미지 주소는 파일이 저장되는 경로를 입력해도 좋으며, 온라인상의 이미지 url을 찾아서 입력해줘도 된다. <'img'> 태그의 src 속성을 지정하는 방법과 완전히 동일하다.
<style>
    p{
        background-image : url("image/profile.jpg");
    }
</style>
<p style="color:white; height:30vh;">
</p>
하지만 잘려나간 부분은 높이가 안맞아서 그런것이다.
<style>
    p{
        background-image: url("image/profile.jpg");
        background-position-y: -200px;
        background-position-x: 200px;
    }
</style>
<p style="color:white; height:30vh;">
</p>
이 때 background-position-x를 활용하여 이미지의 좌우 위치를, background-position-y를 활용하여 이미지의 상하 위치를 바꿀 수 있다. 너비를 초과한 값이 들어올 경우 추가로 이미지의 끝부분을 복제하여 채워준다. (반복적인 패턴 사용 시 용이하다.)

# 화면에 표시되는 방식을 표현하는 스타일 - visibility, display
[visibility]
<style>
    .first{
        visibility:hidden;
    }
</style>
<img class="first" src="image/profile.jpg" height=100px/>
<img class="second" src="image/profile.jpg" height=100px/>

visibility 스타일 속성을 hidden으로 설정하면, 요소를 화면에서 숨길 수 있습니다. 단, 해당 요소가 차지하는 공간이 사라지지는 않는다. 차리는 차지하지만, 화면에 보이지 않게 되는것이다.
[display]
<hr/> 태그로 삽입된 가로줄 위쪽과 아래쪽을 비교하기 바란다. 위쪽은 사진이 좌우로 배치되어 있으며 아래쪽은 사진이 상하로 배치되어 있다. 위쪽의 사진은 inline 속성을 갖고 있지만 아래쪽 사진은 block 속성을 갖고 있기 때문이다.
<style>
    .first{
        display:inline;
    }
    .second{
        display:block;
    }
</style>
<img class="first" src="image/profile.jpg" height=100px/>
<img src="image/profile.jpg" height=100px/>

<hr/>

<img class="second" src="image/profile.jpg" height=100px/>
<img src="image/profile.jpg" height=100px/>