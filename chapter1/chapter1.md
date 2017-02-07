# 1장에서 나오는 CSS 정리

## @media rule

1. media 타입과 디바이스 종류에 따라서 다른 스타일 시트 룰을 적용하기 위해서 사용하는 방법
2. 체크할 수 있는 것들
   * viewport 의 넓이와 크기
   * device 의 넓이와 크기
3. 사용 방법
   1. CSS
   ```
     @media not|only mediatype and (media feature) {
         CSS-Code;
     }    
   ```
   2. html
   ```html
     <link rel="stylesheet" media="mediatype and|not|only (media feature)" href="mystylesheet.css">
   ```
4. 자세한 내용은 아래 링크 참고  
   http://www.w3schools.com/cssref/css3_pr_mediaquery.asp

## box-sizing

1. width, height를 구할 때 padding, margin, border 를 포함할지 않할지를 결정해준다.
2. Default는 padding, margion, border를 포함하지 않는 **content-box**이다.
3. 만약 다 포함하고 싶은 경우는 **border-box**를 이용한다.
4. 이전 버전의 브라우저에서도 동작하기 위해 -moz-, -webkit- 등의 접두어를 붙여서 사용하기도 한다.
5. 자세한 내용은 아래 링크 참고  
   http://www.w3schools.com/cssref/css3_pr_box-sizing.asp

## :after, :before(Pseudo-Elements)

1. Element의 특정 부분에 스타일을 적용하기 위해서 사용
2. ::after
   * Element의 앞 부분에 추가
   * content 라는 속성을 이용해서 내용 등록 가능
3. ::before
   * Element의 뒷 부분에 추가
   * content 라는 속성을 이용해서 내용 등록 가능
4. 그 외의 것은 아래 링크 참고  
   http://www.w3schools.com/css/css_pseudo_elements.asp

## float

1. 특정 Element나 Box를 붕붕 띄워주는 역할을 한다.
2. 주의 사항은 postion: absolute; 옵션이 있는 경우에 해당 부분은 무시된다.
3. float 된 element 이후에 있는 element의 경우 float 된 element의 영역을 첨범하게 된다.(왜냐하면 붕붕 떠다니니깐.) 이 것을 방지하기 위해 clear 속성을 사용한다.
4. 자세한 내용은 아래 링크 참고  
   http://www.w3schools.com/cssref/pr_class_float.asp

## clear

1. 특정 부분에 있는 float 된 element를 침범하지 않도록 설정
2. 속성
   * left: 왼쪽 부분에 있는 element를 침범하지 않도록 설정
   * right: 오른 쪽 부분에 있는 element를 침범하지 않도록 설정
   * boath: 양쪽 다
3. 자세한 내용은 아래 링크 참고  
   http://www.w3schools.com/cssref/pr_class_clear.asp

## margin과 padding

![마진과 패딩](https://i.stack.imgur.com/PeSIJ.gif)

## position

1. element의 positioning method 의 종류를 결정해준다.
2. static: 기본 값, 특별한 기능은 없고 순서대로 위치를 잡아줍니다.
3. relative: 현재 위치를 기반으로 left, top 등을 설정된 값으로 이동을 시켜줍니다. left, top이 없을 경우는 static과 동일하게 동작합니다.
4. absolute: 상위 문서의 position이 relative 인 경우 상위 문서를 기반으로 left, top 등을 설정한 값으로 이동합니다. 만약 상위 문서가 static인 relative 인 문서를 찾아서 그 문서 기반으로 움직이고 없으면 Document 기반으로 해서 움직입니다.
5. fixed: 현재 문서 기반으로 위치를 잡아줍니다. 스크롤을 내리거나 올리더라도 위치는 그대로 있습니다.
6. 자세한 내용은 아래 링크 참고  
   http://www.w3schools.com/cssref/pr_class_position.asp

# 그래픽스 시스템, 랜더링 시스템

## 그래픽스 시스템

1. 그래픽스 : 시각화.
2. 컴퓨터 그래픽스는 점 찍는거..
3. Fixed Number -> 가장 원시적인 그래픽스 시스템
   1. 업데이트 Hell
   2. 힘들다! 하나 씩 다 만들어줘야 하니깐
4. Context --> 먼가 비슷한거 같애..
5. 추상화 계산기!
6. 남이 만들어놓을 것을 쓴다.. --> Components System
7. 프레임워크 --> Components 를 좀 더 추상화!!

8. 이 책은 추상화 개념과 Components 개념을 배운다!

## 랜더링 시스템

1. 렌더링(Rendering) : 시각화되지 않는 것을 시각화해주는 것
2. Geometry Caculate!
3. 공간을 어떻게 나눌까 고민 !
4. 색깔 체우기! --> Fragment(pixcel) Fill!
5. html rendering은 text에 강하다.
6. html component는 form에 강하다.

# 책 내용

1. 레이아웃 : 내가 원하는 컨텐츠를 어떻게 배치할지 정하는 것, 영역을 잡는 것, 관계를 설정하는 것
2. html --> 인쇄가 어떻게 될지 기술하는 언어
   1. 4.0 때 다른 생각을 했다.. => 테그를 사용할 때 의미를 부여하자..
   2. 문서에는 의미가 있어야 한다.. ==> b ==> strong, i ==> information 등등
   3. 테그는 오직 의미로만, 스타일시트를 이용해서 시각화 구성
3. div, span ==> 이건 css를 통해서 먼가를 만들기 위한 의미 없는 테그
4. class?
   1. css 가 테그를 찾기 쉽게 도와주기 위한 방법(selector)으로 제공
   2. 공통점을 강제로 그룹화해서 지정
   3. 각각의 스타일과 selector를 합쳐 놓은 것을 rules
   4. rule들을 모아 놓은 것을 ruleset
   5. ruleset 들을 모아 놓은 것을 sheet
   6. 계속 overide 가능
5. 테그는 의미만 있는 것을 사용해야 한다!!!!
6. 기본적으로 자식 속성은 부모 속성을 상속받는다.(cacading)
7. 긴놈이 이긴다.(.boxA 보다 div.boxA 가 더 길기 떄문에 div.boxA가 이긴다!)
8. 자신을 직접 구현한 것이 이긴다!
9. block: 부모가 허용하는한 될 수 있는한 가로를 가득 채운 것!(기본 테그 : div)
10. inline: 앞에 있는 요소에 같은 배이스 요소로 다음 문자를 적는다.. 인라인 요소 중에서 가장 긴 게 가로 길이 적용
11. inline-block: 
12. display: block과 inline을 구성할 수 있는 속성.
13. float: 화면 크기에 대응하는 스타일을 맞출 때 좋다!
   1. float 아닌 것들 : block, inline ==> 실체(공간을 점유하고 있는 애들!)
   2. 실체가 아니다.(fixed, absolute, float)
   3. block 에게는 별다른 영향을 주지 않는다.(block은 float를 인식하지 못함)
   4. inline 에게는 가드 OR 가이드로 작동한다.

 
