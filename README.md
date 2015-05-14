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
3. 컬럼 세개중 좌우는 고정 중간은 윈도우 크기에 따라 가변적으로 움직임

  참조 : http://www.pagecolumn.com/liquidfixed/3_col_fix-liquid-fix.htm

  이 경우는 먼저 중간 Element를 코드상으로는 배치하고 left 의 margin-left:-100% 로 두는 부분이 인상적임

  HTML 코드의 경우
  ```
  <div id="wrapcenter">
    <div id="center">
      <b>Content Column: <em>Fluid</em></b> </div>
    </div>

    <div id="left">
      <strong>Right Column:</strong> <em id="wleft">230px</em>
    </div>
    <div id="right">
      <strong>Right Column:</strong> <em id="wright">200px</em>
    </div>
  </div>
  ```
  CSS 의 경우

  ```
  #wrapcenter {
    float: left;
    width: 100%;
  }
  #center {
    margin-right: 210px;
    margin-left: 240px;
    background-color: #afeeee;
    height: 200px;
  }
  #left {
    float: left;
    width: 230px;
    margin-left: -100%;
    background: #cfcfcf;
    height: 200px;
  }
  #right {
    float: left;
    width: 200px;
    margin-left: -200px;
    background: #cfcfcf;
    height: 200px;
  }
  ```
