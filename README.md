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

        

    
    
    

#   p l a y - g r o u n d - s c s s  
 