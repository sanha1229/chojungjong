# chojungjong
한글 초성, 중성, 종성 분리 및 결합

## Copyright
© 2021 Sanha, all rights reserved.

## 지원 언어
- JavaScript
- Python (미완성)
- php (미완성)
- Java

## JavaScript

### 시작하기

#### 모듈 불러오기
```javascript
const cjj = require(PATH);
```

### 분리

#### separate(letter: string)
separate 함수는 한글 한 글자를 매개변수로 받아서 초성, 중성, 종성으로 분리한 배열을 반환합니다.
<br><strong>이때, 'ㅇ'도 초성으로 취급됩니다.</strong>
```javascript
cjj.separate('와'); // [ "ㅇ", "ㅗ", "ㅏ" ]
cjj.separate('우'); // [ "ㅇ", "ㅜ", "" ]
```

#### sfa(word: string)
sfa는 **s**eparate into **f**ragment **a**rray의 줄임말로, 이 함수는 한글 여러 글자를 매개변수로 받아서 초성, 중성, 종성으로 분리한 배열의 배열을 반환합니다. 
<br>**이때, 'ㅇ'도 초성으로 취급됩니다.**
```javascript
cjj.sfs('안녕'); // [ [ "ㅇ", "ㅏ", "ㄴ" ], [ "ㄴ", "ㅕ", "ㅇ" ] ]
```

### 결합

#### concat(frag: array)
concat 함수는 초성, 중성, 종성이 담긴 배열을 매개변수로 받아서 한 글자로 결합한 문자열을 반환합니다.
<br>**이때, 초성이 없을 경우에는 대신 'ㅇ'을 사용해야합니다.**
```javascript
cjj.concat(['ㄱ', 'ㅜ', 'ㄱ']); // "국"
cjj.concat(['ㅇ', 'ㅓ']); // "어"
```

#### cfa(fragment: array)
cfa는 **c**oncatenate **f**ragment **a**rray의 줄임말로, 이 함수는 초성, 중성, 종성이 담긴 배열들의 배열을 매개변수로 받아서 각각 결합한 문자열을 반환합니다.
<br>**이때, 초성이 없을 경우에는 대신 'ㅇ'을 사용해야합니다.**
```javascript
cjj.cfa([['ㅎ', 'ㅏ', 'ㄴ'], ['ㄱ', 'ㅡ', 'ㄹ']]); // "한글"
```

#### cfs(fragString: string)
cfs는 **c**oncatenate **f**ragment **s**tring의 줄임말로, 이 함수는 초성, 중성, 종성이 분리된 상태의 문자열을 매개변수로 받아서 각각 결합한 문자열을 반환합니다.
<br>**이때, 초성이 없을 경우에는 대신 'ㅇ'을 사용해야합니다.**
```javascript
cjj.cfs('ㅇㅏㄴㄴㅕㅇㅎㅏㅅㅔㅇㅛ'); // "안녕하세요"
```

## Java
[java](https://github.com/sweetcorn1229/chojungjong/blob/main/src/chojungjongJava/README.md)
