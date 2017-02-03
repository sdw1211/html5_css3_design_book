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
2. static: 기본 값으로 순서에 맞게 표시
3. absolute: 상위 static 하지 않은 element를 중심으로 위치를 잡는다?(흠 설명하기 힘들구만..)
4. fixed: 문서 기반으로 위치 고정
5. relative: Element의 현재 포지션을 기반으로 위치를 잡는다.
6. 자세한 내용은 아래 링크 참고  
   http://www.w3schools.com/cssref/pr_class_position.asp
