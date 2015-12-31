miniUnicode
==

code-golfed Unicode slideshows

Inspired by [this video](https://vimeo.com/36132600) and [this video](https://vimeo.com/48858289)

<br>

64b
---

*Shows all Unicode characters in the page's title*

- [ES6 version](http://xem.github.io/miniUnicode/0-es6.html) (62 bytes)

    i=0;setInterval('document.title=String.fromCodePoint(i++)',99)

128b
---

*Slideshow with all Unicode characters.*
<br>
*Characters: 1114111*
<br>
*Duration: ~25h15*

- [ES6 version](http://xem.github.io/miniUnicode/1-es6.html) (117 bytes) >> [tweet](https://twitter.com/MaximeEuziere/status/680093592598245376)
- [ES5 version](http://xem.github.io/miniUnicode/1-es5.html) (164 bytes) >> [tweet](https://twitter.com/MaximeEuziere/status/680290363077189632)

    <center style="font:50vh/90vh arial"id=a><script>i=0;setInterval('a.innerHTML=String.fromCodePoint(i++)',99)</script>


256b
---

*Slideshow with all Unicode characters and their code points.*

- [ES6 version](http://xem.github.io/miniUnicode/2-es6.html) (208 bytes) >> [codepen](http://codepen.io/xem/pen/WroRxN)
- [ES5 version](http://xem.github.io/miniUnicode/2-es5.html) (251 bytes) >> [codepen](http://codepen.io/xem/pen/dGONMe)

    <center id=u><script>i=0;setInterval('u.innerHTML="<div style=\'height:90vh;font:50vh/90vh arial\'>"+String.fromCodePoint(i)+"</div><b>U+"+(1E9+i.toString(16).toUpperCase()).slice((65536>i++)-5)',99)</script>


512b
---

*Slideshow with just the Unicode [8.0 assigned characters](http://www.unicode.org/Public/UNIDATA/Blocks.txt) and their code points.*
<br>
*[How we golfed the Unicode 8.0 blocks ranges in just 210b](view-source:http://xem.github.io/miniUnicode/3-ranges.html)
<br>
*Characters: 119792*
<br>
*Duration: ~3h20*

- [ES6 version](http://xem.github.io/miniUnicode/3-es6.html) (472 bytes)
- [ES5 version](http://xem.github.io/miniUnicode/3-es5.html) (534 bytes)

    <center id=u><script>i=q=r=0;setInterval('w="86JG3eJG32GP8H10O0NG6HQKMOG8NQILJG2HUKKING6HG8H5IG0G0LPTHKIJG6LGcJK0K5PbJ3UdH8H18H7LRI7PJ06G0Q0QG35H5QNNLbS5TK2G0G0P0L0P6eHH7bH95H2Q05eNNU".replace(/[G-U]/g,a=>-9+(a.charCodeAt(0)-70).toString(16)).split(-9);u.innerHTML="<div style=\'height:90vh;font:50vh/90vh arial\'>"+String.fromCodePoint(i)+"</div><b>U+"+(1E9+i.toString(16).toUpperCase()).slice((65536>i++)-5);++q=="0x"+w[r]+0|0&&(i+="0x"+w[r+1]+0|0,r++,q=0)',99)</script>
