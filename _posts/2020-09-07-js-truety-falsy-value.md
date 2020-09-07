---
layout: post
title:  "[js]자바스크립트 참 같은 값(truety) 거짓 같은 값(falsy)"
description: 자바스크립트에서 참으로 판단되는 값(truety value)과 거짓으로 판단되는 값(falsy value)을 알아보자.
tags: Javascript, js, 자바스크립트, truety, falsy, 참, 거짓,  참 같은 값, 거짓 같은 값
---

Javascript 조건절, 반복문 등 불리언 값이 필요한 곳에서 형 변환을 이용해 특정 값을 불리언 값으로 변환한다.


참 같은 값(truety value): Boolean 문맥에서 참 값으로 판단되는 값


거짓같은 값(falsy value): Boolean 문맥에서 거짓 값으로 판단되는 값




## falsy value

* 0 or -0 : 숫자 zero, 음수 zero
* 0n : BigInt
* '' : 빈 string
* `null` : 아무런 값도 없음
* `undefined` : undefined - 원시값
* `NaN` : NaN - 원시값




## truety value

falsy value 를 제외한 모든 값

* 1 : 숫자
* '비어있지 않은 문자열'
* { k: 1 } : 비어있지 않은 객체
* [1, 2, 3] : 비어있지 않은 배열
* {} : 빈 객체
* [] : 빈 배열

```javascript

function isTruthy(val){
    if(val){
        console.log(val + ' is Truthy');
    }else{
        console.log(val + ' is falsy');
    }
}


// truthy
isTruthy (true)
isTruthy ({})
isTruthy ([])
isTruthy (42)
isTruthy ("0")
isTruthy ("false")
isTruthy (new Date())
isTruthy (-42)
isTruthy (12n)
isTruthy (3.14)
isTruthy (-3.14)
isTruthy (Infinity)
isTruthy (-Infinity)

// falsy
isTruthy(0);
isTruthy("");
isTruthy(false);
isTruthy(NaN);
isTruthy(null);
isTruthy(undefined);

```