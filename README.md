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

```js
el.setAttribute('data-key', 'v'); 
el.getAttribute('data-key'); 
```

~~~js
el.dataset.key = 'v'; 
el.dataset.key; 
~~~

```js
fucntio repaint(el) {
    el.className = el.className; 
}
```


## SASS (SCSS)

- 브라우저에서 컴파일 하기 : https://www.sassmeister.com/
- 즐겨찾기 (학습)
    - https://gist.github.com/jareware/4738651

```scss
@mixin clear {
    zoom: 1; 
    &:after {
        content: " "; 
        display: block; 
        clear: both;
    }
}

@mixin hidetxt {
    position: absolute; 
    visibility: hidden;
    text-indent: -9999em;
}

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

@mixin to-button {
    display: inline-block; 
    text-align: center; 
}

@mixin clear-

@mixin vertical-px($px) {
    position: relative; 
    top: $px;
}

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


## 검색어 

- MDN CSS Selectors
