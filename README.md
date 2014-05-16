## IBG

**a inline-block grids**

[DEMO](http://lvwzhen.github.io/IBG/)

![image](screenshot.png)

###Usage

**HTML**

```html
<div class="container">
	<div class="row">
    	<div class="g-1">grid-1</div>
        ...
        <div class="g-1">grid-1</div>    
    </div>
</div>
```

**CSS**

```css
.row {
    font-size:0;/* 所有浏览器 */
    *word-spacing:-1px;/* IE6、7 */
}
.row [class^="g-"]{
    vertical-align:top;
    word-spacing: normal;
    letter-spacing: normal;
    font-size: 14px;
}
@media screen and (-webkit-min-device-pixel-ratio:0){
/* firefox 中 letter-spacing 会导致脱离普通流的元素水平位移 */
     .row{
            letter-spacing:-5px;/* Safari 等不支持字体大小为 0 的浏览器, N 根据父级字体调节*/
    }
}

@media(min-width: 992px){

    [class^="g-"] {
    display: inline-block;
    *display:inline;
    *zoom:1;
    }

    .g-12 {
         width: 100%
    }

    .g-11 {
        width: 91.66666666666666%
    }

    .g-10 {
        width: 83.33333333333334%
    }
    ...
    
    .g-1 {
        width: 8.333333333333332%
    } 
}
```

## MIT license

The MIT License (MIT)

Copyright (c) 2014 lvwzhen

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
