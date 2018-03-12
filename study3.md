

Lesson 03

**함수단위 코딩 vs . 클래스 단위 코딩**



```javascript
function funcStyle(){

console.log('함수타입 코딩');

}

funcStyle();
funcStyle();
funcStyle();
```



```javascript
//클래스 단위 코딩 (프로토타입)
function classStyle(){
}

classStyle.prototype.classFunction = function(){

console.log('클래스 단위 코딩');

}

$(document).ready(function(){
    var classType = new classStyle();
    
    classType.classFunction();
    classType.classFunction();
    classType.classFunction();

});
```

1. 함수 호출할때마다 함수가 계속 만들어지면서 용량의 과부하를 일으

2. 클래스 이론은 생성을 하고 클래스의 함수를 공유하여 호출하는 방식

   <img src="http://darling2.cafe24.com/study/javascript/study/img/day2/1.JPG" alt="함수방식" />



<img src="http://darling2.cafe24.com/study/javascript/study/img/day2/2.JPG" alt="클래스방식" />

  

```javascript
<script>

  /*
 예제 02: 함수 단위 코딩 방식으로 만들어진 탭메뉴에기능 추가하기
 */
 $(document).ready(function(){
    var tab1 = tabMenu("#tabMenu1");
      // 1번째 탭메뉴 아이템 선택
       tab1.setSelectItemAt(1);

       var tab2 = tabMenu("#tabMenu2");
       // 2번재 탭메뉴 아이템 선택
       tab2.setSelectItemAt(2);

    });

   function tabMenu(selector){
       var $tabMenu =null;
       var $menuItems=null;
       var $selectMenuItem=null;

       // 요소 초기화
      function init(selector){
            $tabMenu = $(selector);
            $menuItems = $tabMenu.find("li");
        }

       // 이벤트 등록
      function initEvent(){
           $menuItems.on("click",function(){
                setSelectItem($(this));
          });
       }

    // $menuItem에 해당하는 메뉴 아이템 선택하기
      function setSelectItem($menuItem){
          // 기존 선택메뉴 아이템을 비활성화 처리하기
          if($selectMenuItem){
             $selectMenuItem.removeClass("select");
          }

         // 신규 아이템 활성화 처리하기
         $selectMenuItem = $menuItem;
         $selectMenuItem.addClass("select");
       }

     // index에 해당하는 메뉴 아이템 선택하기
     function setSelectItemAt(index){
          // setSelectItem() 호출
            setSelectItem($menuItems.eq(index));
	   }

      // 초기화 함수 호출
      init(selector);
      initEvent();

       // 기능 리턴
      return  {
           "setSelectItemAt":setSelectItemAt
        }
   	 }

</script>
```

함수 단위 코딩의 단점을 프로토타입 방식으로 작업할 경우 단점 해결

단점 : 

1. tabMenu() 함수를 호출할 때마다 내부에 선언된 중첩 함수가 만들어집니다.

해결책 -> 프로토타입 방식의 경우 여러 갱의 인스턴스에서 메서드를 공유해서 사용하기 때문에 단점 1 해결

2. 외부에서 내부 속성과 함수를 접근할 수 없습니다.

해결책-> 함수와 달리 프로퍼티와 메서드는 외부에서 접근할 수 있는 구조로 되어 있기 때문에 언제든지 필요한 메서드를 접근해서 사용할 수 있습니다.
