# dropdown메뉴 만들기

## 1. preview

<img src="https://j.gifs.com/2xPnBj.gif" />


## 2. 코드 분석

### 1) html

#### (1) 하나의 div에 button, a태그의 부모인 div를 자식 요소로 둔다.
```html
<body>
    <div class="dropdown">
      <button class="dropdown-btn">Real Esate Type</button>
      <div class="dropdown-submenu">         <!--a태그들을 담는 부모요소 -->
        <a href="#none">ALL</a>
        <a href="#none">OTHER</a>
        <a href="#none">HIGHLIGHT</a>
      </div>
    </div>
  </body>
```

<br/><br/>

### 2) css

#### (1) button에 hover시 dropdown-submenu가 나타나게 한다.
- `hover`전에는 `dropdown-submenu`의 `display:none`이다.
- `button`에 `hover`시 `dropdown-submenu`의 `display:block`이 된다.

```css

a {
  color: #222;               /*a태그 디자인*/
  text-decoration: none;
}
.dropdown-btn {              /*버튼 디자인*/
  width: 200px;
  padding: 10px;
  font-size: 18px;
  background-color: yellowgreen;
  color: #fff;
  border: none;             /*html자체에 있는 border같은 겉선을 제거함*/
}

.dropdown-submenu {
  display: none;                                 /*안보이게*/
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.17);      /*박스에 그림자를 준다.*/
  width: 200px;
  text-align: center;
}
.dropdown-submenu a {
  display: block;                               /*세로로 일렬로 나열*/
}

/* dropdown에 hover가 되면 -> dropdown-submenu에서 무언가가 실행 */
/* hover다음에 나오는 요소는 자식요소여야 함 */
.dropdown:hover .dropdown-submenu {
  display: block;
}
```














