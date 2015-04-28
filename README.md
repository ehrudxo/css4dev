#CSS4dev

1. align to right bottom in certain div(어떤 div 에 오른쪽 아래에 정렬하기)

  감싸고 있는 div(screen) 의 position 을 relative 로 내부 div(innerDiv) 의 position 은 absolute로 놓는 것.이 포인트.
  ```
  <div class="screen">
     <!-- code -->
     <div class="innerdiv">
        text or other content
     </div>
  </div>

  .screen{
  position: relative;
  }
  .innerdiv {
  position: absolute;
  bottom: 0;
  right: 0;
  }

  ```

2. Stretching Div Height as inner divs(내부 div 의 사이즈에 따라서 감싸고 있는 div 사이즈가 늘어나도록 하는 경우)

  감싸고 있는 div(screen) 의 display를 inline-block을 두는 것.
  ```
  <div class="screen">
     <!-- code -->
     <div class="innerdiv">
        text or other content
     </div>
  </div>

  .screen{
    display: inline-block;
  }

  ```
