miniUnicode
==

code-golfed Unicode slideshows

Inspired by [this video](https://vimeo.com/36132600) and [this video](https://vimeo.com/48858289)

<br>

JS1k edition
---

- [Featuring a menu + all assigned blocks](http://xem.github.io/miniUnicode/js1k.min.pack.html) (1024b, ES5)



<br>

Nano (< 64b)
---

*Shows all Unicode characters in the page's title*

- [ES6 version](http://xem.github.io/miniUnicode/0-es6.html) (62 bytes) >> [tweet](https://twitter.com/MaximeEuziere/status/682562455264952320)

````js
i=0;setInterval('document.title=String.fromCodePoint(i++)',99)
````

Micro (< 128b)
---

*Slideshow with all Unicode characters.*
<br>
*Characters: 1114111*
<br>
*Duration: ~25h15*

- [ES6 version](http://xem.github.io/miniUnicode/1-es6.html) (110 bytes) >> [tweet](https://twitter.com/MaximeEuziere/status/680093592598245376)
- [ES5 version](http://xem.github.io/miniUnicode/1-es5.html) (164 bytes) >> [tweet](https://twitter.com/MaximeEuziere/status/680290363077189632)

````html
<center style=font:45vh/2'arial' id=a><svg onload=i=0;setInterval('a.innerHTML=String.fromCodePoint(i++)',99)>
````

Mini (< 256b)
---

*Slideshow with all Unicode characters and their code points.*

- [ES6 version](http://xem.github.io/miniUnicode/2-es6.html) (208 bytes) >> [codepen](http://codepen.io/xem/pen/WroRxN)
- [ES5 version](http://xem.github.io/miniUnicode/2-es5.html) (251 bytes) >> [codepen](http://codepen.io/xem/pen/dGONMe)

````html
<center id=u><script>i=0;setInterval('u.innerHTML="<div style=\'height:90vh;font:50vh/90vh arial\'>"+String.fromCodePoint(i)+"</div><b>U+"+(1E9+i.toString(16).toUpperCase()).slice((65536>i++)-5)',99)</script>
````

Big (~ 512b)
---

*Colored slideshow with just the [Unicode 8.0 assigned characters](http://www.unicode.org/Public/UNIDATA/Blocks.txt) and their code points.*
<br>
*Here's [how we golfed the Unicode 8.0 blocks ranges in just 210b](http://xem.github.io/miniUnicode/3-ranges.html)*
<br>
*Characters: 119,792*
<br>
*Duration: ~3h20*

- [ES6 version](http://xem.github.io/miniUnicode/3-es6.html) (560 bytes)
- [ES5 version](http://xem.github.io/miniUnicode/3-es5.html) (621 bytes)

````html
<body id=u><script>i=q=r=0;k='style="font:4';setInterval('u.'+k+'vh arial;color:#fff;background:hsl("+(i/9+200)+",80%,50%)";w="86JG3eJG32GP8H10O0NG6HQKMOG8NQILJG2HUKKING6HG8H5IG0G0LPTHKIJG6LGcJK0K5PbJ3UdH8H18H7LRI7PJ06G0Q0QG35H5QNNLbS5TK2G0G0P0L0P6eHH7bH95H2Q05eNNU".replace(/[G-U]/g,a=>-9+(a.charCodeAt()-70).toString(16)).split(-9);u.innerHTML=\'<center><div '+k+'5vh/85vh arial;height:85vh">\'+String.fromCodePoint(i)+"</div><b>U+"+(1E9+i.toString(16).toUpperCase()).slice((65536>i++)-5);++q=="0x"+w[r]+0|0&&(r++,i+="0x"+w[r++]+0|0,r++,q=0)',99)</script>
````


Huge (< 4kb)
---

*Colored slideshow with Unicode 8.0, code points and blocks names*

- [ES6 + RegPack version](http://xem.github.io/miniUnicode/4-es6.html) (3483 bytes)
- [ES6 version](http://xem.github.io/miniUnicode/4-es6.html) (5278 bytes)
- [ES5 version](http://xem.github.io/miniUnicode/4-es5.html) (5336 bytes)

````html
<body id=u><script>i=q=r=0;setInterval('w="8,N,N,S,L,K,M,O,G0,I,L,M,G0,K,I,J,J,J,HJL,N,N,N,N,N,N,N,N,N,N,N,N,G0,P,L,G0,G8,H,L,H8,H,L,H,H,H,H,N,Q,K,K,I,L,H,H,O,K,N,J,J,K,IJG,I,N,J,J,G0,G0,M,I,I,I,K,J,M,G0,G0,J,H,P,N,H,L,G0,R,I,G,G0,N,N,G0,G0,L,H,N,I,K,L,H,N,N,TGG,J,L,L,I,L,G,H,I,G,G0,G0,G9c,J,K20,J9,J,I,G4,L,L,H,T,I,G,J,L,H,I,I,H,L,H,L,H,L,H,I,J,K,J,Hbb,KH10H0,K,Hb,G,G,G,H,H,O,U,G,N,N,J,K,J,INH,J,H,I,H,I,H,JHK,I,IKI,JOG8NJ,H,H,IIH,H,HJH,L,L,H,HHJ,J,H,H,IKKING6HG8N,K,I,K,I,L,H,KII,K,NG0LPN,LHKIJG6LGcJK0J0,N,SPbJ3UdH8H18H4,ILI,OI7PJ06G0Q0P,GG35G0,G0,KQL,HNJ0,HbS5TK2G0G0I,M,L,G0,G0,I0,K,I,N,N,N,G0,G0L0P6eHG04,T,G69H95H2Q05eNNU".replace(/[G-U]/g,a=>","+(a.charCodeAt()-70).toString(16)).split(",");A="BASIC LATIN0LATIN-1 SUPPLEMENT0LATIN EXTENDED-A0LATIN EXTENDED-B0IPA EXTENSIONS0SPACING MODIFIER LETTERS0COMBINING DIACRITICAL MARKS0GREEK AND COPTIC0CYRILLIC0CYRILLIC SUPPLEMENT0ARMENIAN0HEBREW0ARABIC0SYRIAC0ARABIC SUPPLEMENT0THAANA0NKO0SAMARITAN0MANDAIC0ARABIC EXTENDED-A0DEVANAGARI0BENGALI0GURMUKHI0GUJARATI0ORIYA0TAMIL0TELUGU0KANNADA0MALAYALAM0SINHALA0THAI0LAO0TIBETAN0MYANMAR0GEORGIAN0HANGUL JAMO0ETHIOPIC0ETHIOPIC SUPPLEMENT0CHEROKEE0UNIFIED CANADIAN ABORIGINAL SYLLABICS0OGHAM0RUNIC0TAGALOG0HANUNOO0BUHID0TAGBANWA0KHMER0MONGOLIAN0UNIFIED CANADIAN ABORIGINAL SYLLABICS EXTENDED0LIMBU0TAI LE0NEW TAI LUE0KHMER SYMBOLS0BUGINESE0TAI THAM0COMBINING DIACRITICAL MARKS EXTENDED0BALINESE0SUNDANESE0BATAK0LEPCHA0OL CHIKI0SUNDANESE SUPPLEMENT0VEDIC EXTENSIONS0PHONETIC EXTENSIONS0PHONETIC EXTENSIONS SUPPLEMENT0COMBINING DIACRITICAL MARKS SUPPLEMENT0LATIN EXTENDED ADDITIONAL0GREEK EXTENDED0GENERAL PUNCTUATION0SUPERSCRIPTS AND SUBSCRIPTS0CURRENCY SYMBOLS0COMBINING DIACRITICAL MARKS FOR SYMBOLS0LETTERLIKE SYMBOLS0NUMBER FORMS0ARROWS0MATHEMATICAL OPERATORS0MISCELLANEOUS TECHNICAL0CONTROL PICTURES0OPTICAL CHARACTER RECOGNITION0ENCLOSED ALPHANUMERICS0BOX DRAWING0BLOCK ELEMENTS0GEOMETRIC SHAPES0MISCELLANEOUS SYMBOLS0DINGBATS0MISCELLANEOUS MATHEMATICAL SYMBOLS-A0SUPPLEMENTAL ARROWS-A0BRAILLE PATTERNS0SUPPLEMENTAL ARROWS-B0MISCELLANEOUS MATHEMATICAL SYMBOLS-B0SUPPLEMENTAL MATHEMATICAL OPERATORS0MISCELLANEOUS SYMBOLS AND ARROWS0GLAGOLITIC0LATIN EXTENDED-C0COPTIC0GEORGIAN SUPPLEMENT0TIFINAGH0ETHIOPIC EXTENDED0CYRILLIC EXTENDED-A0SUPPLEMENTAL PUNCTUATION0CJK RADICALS SUPPLEMENT0KANGXI RADICALS0IDEOGRAPHIC DESCRIPTION CHARACTERS0CJK SYMBOLS AND PUNCTUATION0HIRAGANA0KATAKANA0BOPOMOFO0HANGUL COMPATIBILITY JAMO0KANBUN0BOPOMOFO EXTENDED0CJK STROKES0KATAKANA PHONETIC EXTENSIONS0ENCLOSED CJK LETTERS AND MONTHS0CJK COMPATIBILITY0CJK UNIFIED IDEOGRAPHS EXTENSION A0YIJING HEXAGRAM SYMBOLS0CJK UNIFIED IDEOGRAPHS0YI SYLLABLES0YI RADICALS0LISU0VAI0CYRILLIC EXTENDED-B0BAMUM0MODIFIER TONE LETTERS0LATIN EXTENDED-D0SYLOTI NAGRI0COMMON INDIC NUMBER FORMS0PHAGS-PA0SAURASHTRA0DEVANAGARI EXTENDED0KAYAH LI0REJANG0HANGUL JAMO EXTENDED-A0JAVANESE0MYANMAR EXTENDED-B0CHAM0MYANMAR EXTENDED-A0TAI VIET0MEETEI MAYEK EXTENSIONS0ETHIOPIC EXTENDED-A0LATIN EXTENDED-E0CHEROKEE SUPPLEMENT0MEETEI MAYEK0HANGUL SYLLABLES0HANGUL JAMO EXTENDED-B0CJK COMPATIBILITY IDEOGRAPHS0ALPHABETIC PRESENTATION FORMS0ARABIC PRESENTATION FORMS-A0VARIATION SELECTORS0VERTICAL FORMS0COMBINING HALF MARKS0CJK COMPATIBILITY FORMS0SMALL FORM VARIANTS0ARABIC PRESENTATION FORMS-B0HALFWIDTH AND FULLWIDTH FORMS0SPECIALS0LINEAR B SYLLABARY0LINEAR B IDEOGRAMS0AEGEAN NUMBERS0ANCIENT GREEK NUMBERS0ANCIENT SYMBOLS0PHAISTOS DISC0LYCIAN0CARIAN0COPTIC EPACT NUMBERS0OLD ITALIC0GOTHIC0OLD PERMIC0UGARITIC0OLD PERSIAN0DESERET0SHAVIAN0OSMANYA0ELBASAN0CAUCASIAN ALBANIAN0LINEAR A0CYPRIOT SYLLABARY0IMPERIAL ARAMAIC0PALMYRENE0NABATAEAN0HATRAN0PHOENICIAN0LYDIAN0MEROITIC HIEROGLYPHS0MEROITIC CURSIVE0KHAROSHTHI0OLD SOUTH ARABIAN0OLD NORTH ARABIAN0MANICHAEAN0AVESTAN0INSCRIPTIONAL PARTHIAN0INSCRIPTIONAL PAHLAVI0PSALTER PAHLAVI0OLD TURKIC0OLD HUNGARIAN0RUMI NUMERAL SYMBOLS0BRAHMI0KAITHI0SORA SOMPENG0CHAKMA0MAHAJANI0SHARADA0SINHALA ARCHAIC NUMBERS0KHOJKI0MULTANI0KHUDAWADI0GRANTHA0TIRHUTA0SIDDHAM0MODI0TAKRI0AHOM0WARANG CITI0PAU CIN HAU0CUNEIFORM0CUNEIFORM NUMBERS AND PUNCTUATION0EARLY DYNASTIC CUNEIFORM0EGYPTIAN HIEROGLYPHS0ANATOLIAN HIEROGLYPHS0BAMUM SUPPLEMENT0MRO0BASSA VAH0PAHAWH HMONG0MIAO0KANA SUPPLEMENT0DUPLOYAN0SHORTHAND FORMAT CONTROLS0BYZANTINE MUSICAL SYMBOLS0MUSICAL SYMBOLS0ANCIENT GREEK MUSICAL NOTATION0TAI XUAN JING SYMBOLS0COUNTING ROD NUMERALS0MATHEMATICAL ALPHANUMERIC SYMBOLS0SUTTON SIGNWRITING0MENDE KIKAKUI0ARABIC MATHEMATICAL ALPHABETIC SYMBOLS0MAHJONG TILES0DOMINO TILES0PLAYING CARDS0ENCLOSED ALPHANUMERIC SUPPLEMENT0ENCLOSED IDEOGRAPHIC SUPPLEMENT0MISCELLANEOUS SYMBOLS AND PICTOGRAPHS0EMOTICONS0ORNAMENTAL DINGBATS0TRANSPORT AND MAP SYMBOLS0ALCHEMICAL SYMBOLS0GEOMETRIC SHAPES EXTENDED0SUPPLEMENTAL ARROWS-C0SUPPLEMENTAL SYMBOLS AND PICTOGRAPHS0CJK UNIFIED IDEOGRAPHS EXTENSION B0CJK UNIFIED IDEOGRAPHS EXTENSION C0CJK UNIFIED IDEOGRAPHS EXTENSION D0CJK UNIFIED IDEOGRAPHS EXTENSION E0CJK COMPATIBILITY IDEOGRAPHS SUPPLEMENT0TAGS0VARIATION SELECTORS SUPPLEMENT".split(0);u.style="font:4vh arial;color:#fff;background:hsl("+(i/9+200)+",80%,50%)";u.innerHTML=\'<center><div style="font:45vh/85vh arial;height:85vh">\'+String.fromCodePoint(i)+"</div><b>U+"+(1E9+i.toString(16).toUpperCase()).slice((65536>i++)-5)+"<br>"+A[~~(r/2)];++q=="0x"+w[r]+0|0&&(r++,i+="0x"+w[r++]+0|0,q=0)',99)</script>
````


Epic (< 512kb)
---

*Colored slideshow with Unicode 8.0, code points, blocks names and all canonical names (WIP, experimental)*
<br>
*Duration: ~16h40*

- [ES6 version](http://xem.github.io/miniUnicode/5-es6.html) (3,31mb, 347kb gzipped)

````html
<body id=u><script>i=j=q=r=0;w="8,N,N,S,L,K,M,O,G0,I,L,M,G0,K,I,J,J,J,HJL,N,N,N,N,N,N,N,N,N,N,N,N,G0,P,L,G0,G8,H,L,H8,H,L,H,H,H,H,N,Q,K,K,I,L,H,H,O,K,N,J,J,K,IJG,I,N,J,J,G0,G0,M,I,I,I,K,J,M,G0,G0,J,H,P,N,H,L,G0,R,I,G,G0,N,N,G0,G0,L,H,N,I,K,L,H,N,N,TGG,J,L,L,I,L,G,H,I,G,G0,G0,G9c,J,K20,J9,J,I,G4,L,L,H,T,I,G,J,L,H,I,I,H,L,H,L,H,L,H,I,J,K,J,Hbb,KH10H0,K,Hb,G,G,G,H,H,O,U,G,N,N,J,K,J,INH,J,H,I,H,I,H,JHK,I,IKI,JOG8NJ,H,H,IIH,H,HJH,L,L,H,HHJ,J,H,H,IKKING6HG8N,K,I,K,I,L,H,KII,K,NG0LPN,LHKIJG6LGcJK0J0,N,SPbJ3UdH8H18H4,ILI,OI7PJ06G0Q0P,GG35G0,G0,KQL,HNJ0,HbS5TK2G0G0I,M,L,G0,G0,I0,K,I,N,N,N,G0,G0L0P6eHG04,T,G69H95H2Q05eNNU".replace(/[G-U]/g,a=>","+(a.charCodeAt()-70).toString(16)).split(",");A="BASIC LATIN0LATIN-1 SUPPLEMENT0LATIN EXTENDED-A0LATIN EXTENDED-B0IPA EXTENSIONS0SPACING MODIFIER LETTERS0COMBINING DIACRITICAL MARKS0GREEK AND COPTIC0CYRILLIC0CYRILLIC SUPPLEMENT0ARMENIAN0HEBREW0ARABIC0SYRIAC0ARABIC SUPPLEMENT0THAANA0NKO0SAMARITAN0MANDAIC0ARABIC EXTENDED-A0DEVANAGARI0BENGALI0GURMUKHI0GUJARATI0ORIYA0TAMIL0TELUGU0KANNADA0MALAYALAM0SINHALA0THAI0LAO0TIBETAN0MYANMAR0GEORGIAN0HANGUL JAMO0ETHIOPIC0ETHIOPIC SUPPLEMENT0CHEROKEE0UNIFIED CANADIAN ABORIGINAL SYLLABICS0OGHAM0RUNIC0TAGALOG0HANUNOO0BUHID0TAGBANWA0KHMER0MONGOLIAN0UNIFIED CANADIAN ABORIGINAL SYLLABICS EXTENDED0LIMBU0TAI LE0NEW TAI LUE0KHMER SYMBOLS0BUGINESE0TAI THAM0COMBINING DIACRITICAL MARKS EXTENDED0BALINESE0SUNDANESE0BATAK0LEPCHA0OL CHIKI0SUNDANESE SUPPLEMENT0VEDIC EXTENSIONS0PHONETIC EXTENSIONS0PHONETIC EXTENSIONS SUPPLEMENT0COMBINING DIACRITICAL MARKS SUPPLEMENT0LATIN EXTENDED ADDITIONAL0GREEK EXTENDED0GENERAL PUNCTUATION0SUPERSCRIPTS AND SUBSCRIPTS0CURRENCY SYMBOLS0COMBINING DIACRITICAL MARKS FOR SYMBOLS0LETTERLIKE SYMBOLS0NUMBER FORMS0ARROWS0MATHEMATICAL OPERATORS0MISCELLANEOUS TECHNICAL0CONTROL PICTURES0OPTICAL CHARACTER RECOGNITION0ENCLOSED ALPHANUMERICS0BOX DRAWING0BLOCK ELEMENTS0GEOMETRIC SHAPES0MISCELLANEOUS SYMBOLS0DINGBATS0MISCELLANEOUS MATHEMATICAL SYMBOLS-A0SUPPLEMENTAL ARROWS-A0BRAILLE PATTERNS0SUPPLEMENTAL ARROWS-B0MISCELLANEOUS MATHEMATICAL SYMBOLS-B0SUPPLEMENTAL MATHEMATICAL OPERATORS0MISCELLANEOUS SYMBOLS AND ARROWS0GLAGOLITIC0LATIN EXTENDED-C0COPTIC0GEORGIAN SUPPLEMENT0TIFINAGH0ETHIOPIC EXTENDED0CYRILLIC EXTENDED-A0SUPPLEMENTAL PUNCTUATION0CJK RADICALS SUPPLEMENT0KANGXI RADICALS0IDEOGRAPHIC DESCRIPTION CHARACTERS0CJK SYMBOLS AND PUNCTUATION0HIRAGANA0KATAKANA0BOPOMOFO0HANGUL COMPATIBILITY JAMO0KANBUN0BOPOMOFO EXTENDED0CJK STROKES0KATAKANA PHONETIC EXTENSIONS0ENCLOSED CJK LETTERS AND MONTHS0CJK COMPATIBILITY0CJK UNIFIED IDEOGRAPHS EXTENSION A0YIJING HEXAGRAM SYMBOLS0CJK UNIFIED IDEOGRAPHS0YI SYLLABLES0YI RADICALS0LISU0VAI0CYRILLIC EXTENDED-B0BAMUM0MODIFIER TONE LETTERS0LATIN EXTENDED-D0SYLOTI NAGRI0COMMON INDIC NUMBER FORMS0PHAGS-PA0SAURASHTRA0DEVANAGARI EXTENDED0KAYAH LI0REJANG0HANGUL JAMO EXTENDED-A0JAVANESE0MYANMAR EXTENDED-B0CHAM0MYANMAR EXTENDED-A0TAI VIET0MEETEI MAYEK EXTENSIONS0ETHIOPIC EXTENDED-A0LATIN EXTENDED-E0CHEROKEE SUPPLEMENT0MEETEI MAYEK0HANGUL SYLLABLES0HANGUL JAMO EXTENDED-B0CJK COMPATIBILITY IDEOGRAPHS0ALPHABETIC PRESENTATION FORMS0ARABIC PRESENTATION FORMS-A0VARIATION SELECTORS0VERTICAL FORMS0COMBINING HALF MARKS0CJK COMPATIBILITY FORMS0SMALL FORM VARIANTS0ARABIC PRESENTATION FORMS-B0HALFWIDTH AND FULLWIDTH FORMS0SPECIALS0LINEAR B SYLLABARY0LINEAR B IDEOGRAMS0AEGEAN NUMBERS0ANCIENT GREEK NUMBERS0ANCIENT SYMBOLS0PHAISTOS DISC0LYCIAN0CARIAN0COPTIC EPACT NUMBERS0OLD ITALIC0GOTHIC0OLD PERMIC0UGARITIC0OLD PERSIAN0DESERET0SHAVIAN0OSMANYA0ELBASAN0CAUCASIAN ALBANIAN0LINEAR A0CYPRIOT SYLLABARY0IMPERIAL ARAMAIC0PALMYRENE0NABATAEAN0HATRAN0PHOENICIAN0LYDIAN0MEROITIC HIEROGLYPHS0MEROITIC CURSIVE0KHAROSHTHI0OLD SOUTH ARABIAN0OLD NORTH ARABIAN0MANICHAEAN0AVESTAN0INSCRIPTIONAL PARTHIAN0INSCRIPTIONAL PAHLAVI0PSALTER PAHLAVI0OLD TURKIC0OLD HUNGARIAN0RUMI NUMERAL SYMBOLS0BRAHMI0KAITHI0SORA SOMPENG0CHAKMA0MAHAJANI0SHARADA0SINHALA ARCHAIC NUMBERS0KHOJKI0MULTANI0KHUDAWADI0GRANTHA0TIRHUTA0SIDDHAM0MODI0TAKRI0AHOM0WARANG CITI0PAU CIN HAU0CUNEIFORM0CUNEIFORM NUMBERS AND PUNCTUATION0EARLY DYNASTIC CUNEIFORM0EGYPTIAN HIEROGLYPHS0ANATOLIAN HIEROGLYPHS0BAMUM SUPPLEMENT0MRO0BASSA VAH0PAHAWH HMONG0MIAO0KANA SUPPLEMENT0DUPLOYAN0SHORTHAND FORMAT CONTROLS0BYZANTINE MUSICAL SYMBOLS0MUSICAL SYMBOLS0ANCIENT GREEK MUSICAL NOTATION0TAI XUAN JING SYMBOLS0COUNTING ROD NUMERALS0MATHEMATICAL ALPHANUMERIC SYMBOLS0SUTTON SIGNWRITING0MENDE KIKAKUI0ARABIC MATHEMATICAL ALPHABETIC SYMBOLS0MAHJONG TILES0DOMINO TILES0PLAYING CARDS0ENCLOSED ALPHANUMERIC SUPPLEMENT0ENCLOSED IDEOGRAPHIC SUPPLEMENT0MISCELLANEOUS SYMBOLS AND PICTOGRAPHS0EMOTICONS0ORNAMENTAL DINGBATS0TRANSPORT AND MAP SYMBOLS0ALCHEMICAL SYMBOLS0GEOMETRIC SHAPES EXTENDED0SUPPLEMENTAL ARROWS-C0SUPPLEMENTAL SYMBOLS AND PICTOGRAPHS0CJK UNIFIED IDEOGRAPHS EXTENSION B0CJK UNIFIED IDEOGRAPHS EXTENSION C0CJK UNIFIED IDEOGRAPHS EXTENSION D0CJK UNIFIED IDEOGRAPHS EXTENSION E0CJK COMPATIBILITY IDEOGRAPHS SUPPLEMENT0TAGS0VARIATION SELECTORS SUPPLEMENT".split(0);B=["NULL",/* =================== SNIP 119,790 names ================= */,"VARIATION SELECTOR-256"];setInterval('u.style="-moz-control-character-visibility:visible;font:4vh arial;color:#fff;background:hsl("+(i/9+200)+",80%,50%)";u.innerHTML=\'<center><div style="font:40vh/80vh arial;height:80vh">\'+String.fromCodePoint(i)+"</div><b>U+"+(1E9+i.toString(16).toUpperCase()).slice((65536>i++)-5)+"<br>"+A[~~(r/2)]+"<br>"+B[j++];++q=="0x"+w[r]+0|0&&(r++,i+="0x"+w[r++]+0|0,q=0)',200)</script>