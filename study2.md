<h1>day2</h1>

1. 함수를 사용하는 이유를 알고 있나요? ㅇㅇ

- 함수란?  특정기능을 하는 구문(알고리즘,로직)을 묶어 재사용하는 문법입니다. 일종의 포장방법 이라고 말할 수 있음.

- 사용 이유
  소스가 훨씬 더 간결하고 깔끔해짐.

1. 지역변수와 전역변수를 이해하고 있나요? ㅇㅇ
   - 지역변수 ? 특정영역에서만 사용할 수 있는 변수, 주로 함수 내부에 만들어짐
   - 전역변수 ? 전역에서 사용하는 데이터를 담는 변수, 어디서든 접근 가능.

    <script>
    var glo = '전역변수';
    window.onload=function(){
    
    glo2 = '전역변수'; // var 없이 변수에 값을 대입하면 전역변수로 만들어짐. window.glo2='전역변수' 와 같음
    
    }
    function fun1(){
    
    var glo3= '지역변수';
    
    }
    </script>

1. 매개변수가 있는 함수를 만들 수 있나요? ㅇㅇ
   - 매개변수? 일종의 외부 데이터를 함수 내부로 전달하는 매개체 역할을 하는 변수.

     function pr99(i){ //i가 매개변수!
      document.write(i +'x 2 ='+ (i*2),'<br />')
      document.write(i +'x 4 ='+ (i*4));
      }
    
    pr99(5); //데이터 // 매개변수==데이터 같게 된다.!

1. 리턴값이 있는 함수를 만들 수 있나요? ㅇㅇ

     function sum(a,b){
     	var result  = a+b;
     	return result;
     }
     var data = sum(10,20);
     var data = 30;

1. 중첩 함수를 이해하고 있나요? ㅇㅇ
   - 함수 내부에 만들어 지는 함수(하나 이상 생성 가능)

    function sthello(){
      var count = 0;
    
      setInterval (function(){
    
      count++;
      document.write(count + '안녕하세요', '<br>');
    
      },1000)
    }
    
    sthello();

1. 콜백 함수를 이해하고 있나요? ㅇㅇ
   - 함수 내부의 처리 결과값을 함수 외부로 내보낼 때 사용,

    function cal(op,num1,num2,call){
    var result = '';
    switch(op){
    
    case "+" :
    	result = num1 + num2 ;
    	break;
    case "-" :
    	result = num1 - num2;
    	break;
    case "*" :
    	result = num1*num2;
    	break;
    case "/":
    	result =num1/num2;
    	break;
    default :
    	result ='지원하지 않는 연산자';
    
    }
    call(result);
    }
    function prin1(result){
    document.write('두 수의 합은' +result );
    }
    function prin2(result){
    document.write('게싼' +result );
    }
    cal('+',10,20,prin1);  //callback 함수
    cal('*',60,20,prin2);  //callback 함수



7.클로저를 이해하고 있나요?

    function create(){
       var count=0;
       function addCount(){
    
       count++;
       return count;
    
       }
       return addCount;
       }
    
    var counter = create();
    
    document.write(counter()); //1
    document.write(counter()); //2
    document.write(counter()); //3       

8.함수를 이용해 간단한 탭메뉴를 만들 수 있나요? ㄴㄴ
