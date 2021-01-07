# SCSS 설치 
    확장자는 .scss 로 하고 여러가지 컴파일 도구들이 있습니다. 
    그중 parcel 이 가장 간단 하므로 실습 및 테스트 해봅니다. 
    
    글로벌로 설치후 devdependency 로 node-sass 설치 
        npm install -g parcel 
        npm install -save-dev node-sass 

    실행 
        <link style.scss>
        parcel index.html 
        parcel build index.html 
    
    웹 도구 
        https://www.sassmeister.com/

# SCSS 문법 
    중첩 
        .container{ .item { }}
    
    구조화 
        @import 'config'
        main.scss , _header.scss, _aside.scss 
        node-sass scss --output css

    
    변수 및 데이터
        $text-large: 18px;
        font-size : $text-large
    
    변수 우선순위 
    !global
        아래와 같을때 import 처럼 동작 한다. 
        $text-large: 12px
        {
        $text-large: 18px !global;
        }
    !default 초기값 


    상위 선택자 참조 &
        .container{
            &:hover{

            }
        }
    
    중첩 벗어나기 @at-root
        같은 블럭 안에는 있어야 함 
        @at-root.

    중첩 속성 
        font: {
            size:10px;
            weight:700;
        }
    문자 보간
        자바스크립트에서 ${} 이것과 같음 
        #{} 이렇게 사용 

    SCSS to CSS
        npm i node-sass -g
        
        sass 폴더에 있는 sass 파일을 css 폴더로 css 파일 만들기 
        node-sass sass --output css

        만약 파일앞에 _ 가 붙어있다면 한개의 css 파일을 만든다. 

# SCSS 연산 
    사칙 연산             
        + : width: 20px + 30px 
        - : width: 20px - 30px 
        * : width: 20px * 30  단위가 있으면 안됨~! 
        / : width: (20px / 2) 단위가 있으면 안되고, 우선 연산 때문에 () 괄호 사용 

    비교 연산 
        == : 동등 
        != : 부등
        <  : 작음 
        >  : 큰
        <= : 작거나 같음
        >= : 크거나 같음

    불린 연산 
        @if (조건문)
        
        and : 그리고
        or  : 혹은
        not : 부정 

    calc() 연산 
        width : calc(20% + 10px);  이런 연산 가능
        하지만 width : 20% + 10px; 이런 연산 불가!

    문자 연산 
        + 가 사용 되고 첫번째 피연산자가 기준 
        첫번째 피연산자가 "" 따음표 있으면, 연산 결과를 따음표로 묶음. 
                            따음표가 없다면, 연산 결과에 따음표 처리 안함. 

    div::after{
        content : "Hello" + World;   // "Hello World " 로 처리 
        flex: inline + "-flex";   // inline-flex  로 처리 
    }

    색상 연산 
        color : #123456 + #345678;






 