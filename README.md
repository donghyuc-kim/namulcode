# namulcode

```html
<!doctype html>
<meta charset="utf-8">
<title>${title}</title>
<div>가장 간단한 HTML5 마크업</div>
```

```html
<!-- 검색엔진 색인 -->
<meta name="robots" content="noindex, nofollow">
<meta name="googlebot" content="noindex, nofollow">
<!-- IE렌더링 엔진 -->
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

- https://ko.wikipedia.org/wiki/검색_엔진_최적화


```html
<input list="_id">
<datalist id="_id">
    <option value="hello world">
    <option value="donghyuc-kim">
    <option value="soopul">
    <option value="namulcode">
    <option value="html living standard">
    <option value="content modeler">
    <option value="web components">
    <option value="dom script">
</datalist>
```

```html
<details open>
    <summary>...</summary>
    <p>...</p>
    <p>...</p>
</details>
```

## CSS

```css
* {
    -webkit-appearance: none; 
}
```

## SASS (SCSS)

- 브라우저에서 컴파일 하기 : https://www.sassmeister.com/
- 즐겨찾기 (학습)
    - https://gist.github.com/jareware/4738651
    - http://sass-lang.com/documentation/file.SASS_REFERENCE.html

```scss
@mixin clear {
    zoom: 1; 
    &:after {
        content: " "; 
        display: block; 
        clear: both;
    }
}
```

```scss
@mixin hidden {
    position: absolute; 
    visibility: hidden;
    text-indent: -9999em;
}
```

```scss
@mixin ellipsis{
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

@mixin un-ellipsis{
    overflow: auto;
    text-overflow: inherit;
    white-space: inherit;
}

@mixin ellipsis-line($line) {
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: $line; // line number
    -webkit-box-orient: vertical;
    word-wrap: break-word; 
}
```

```scss
@mixin to-button {
    display: inline-block; 
    text-align: center; 
}

@mixin set-action {
    cursor: pointer; 
    -ms-user-select: none; 
    user-select: none; 
}
```

```scss
@mixin vertical-px($px) {
    position: relative; 
    top: $px;
}
```

```scss
$path: 'https://localhost:3000';
@mixin pseudo-icon($name-pseudo, $src, $w:auto, $name-position:'left', $lr:0) {
    &:#{$name-pseudo} {
        content: " "; 
        position: absolute; 
        top: 0; 
        bottom: 0; 
        #{$name-position}: $lr; 
        width: $w; 
        background: transparent url($path + $src) no-repeat center center; 
    }
}
.test--pesudo-icon {
  @include pseudo-icon('after', '/test.png', 20px);
}
```

```scss
.world {
  color: red; 
  
  .hello & {
    display: block; 
  }
}

/* output : */
.world {
  color: red;
}
.hello .world {
  display: block;
}
```

```scss
@mixin mx1() {
  text-decoration: underline; 
}

%ex1 { 
  border: 1px solid red; 
}

.hello { 
  color: red; 
}

.world { 
  @include mx1; 
  @extend .hello; 
  @extend %ex1; 
  text-align: center; 
}

.dev {
  @extend %ex1; 
}

/* output : */
.dev, .world {
  border: 1px solid red;
}

.hello, .world {
  color: red;
}

.world {
  text-decoration: underline;
  text-align: center;
}
```


## javascript 

```js
el.setAttribute('data-key', 'v'); 
el.getAttribute('data-key'); 
```

~~~js
el.dataset.key = 'v'; 
el.dataset.key; 
~~~

```js
function repaint(el) {
    el.className = el.className; 
}
```


## 검색어 

- MDN CSS Selectors
