---
layout: post
title: 파이썬 자료형(숫자형)[Python Number]
image: python.jpg
date: 2021-04-30-01:53
tags: [python, number]
categories: python
---

<details>
<summary>English</summary>
<div markdown="1">

Number is numeric data types, such as integers such as 1, 2, and 3, real numbers such as 3.14, and octal or hexadecimal numbers.<br><br>

|section|example|
|:---:|:---:|
|integer|365, -500, 0|
|real income|3.14, -3.14, 2.8e|
|Octal|0o46, 0o25|
|Hexadecimal|0xF1, 0x3A|
{:.mbtablestyle}
<br><br>

<Blockquote>integer</Blockquote>
As the name implies, the integer type is a data type that means integer.
{% highlight python %}
>>> num = 365
>>> num = -500
>>> num = 0
{% endhighlight %}

<br>
<Blockquote>real income</Blockquote>
A floating-point in Python is a number that contains a decimal point.
{% highlight python %}
>>> num = 3.14
>>> num = -3.14
{% endhighlight %}
The above method is the method we commonly use, but the expressions used by computers are as follows.
{% highlight python %}
>>> num = 3.14e10
>>> num = 3.14E-10
{% endhighlight %}
It doesn't matter if you write e or E.

<br>

<Blockquote>Octal and Hexadecimal</Blockquote>
The octal number can be expressed as 0o (0O is also possible).
{% highlight python %}
>>> num = 0o12
{% endhighlight %}
Hexadecimal numbers are expressed as 0x.
{% highlight python %}
>>> num = 0xFF
>>> num = 0x1A
{% endhighlight %}
Octal or hexadecimal are numeric data types that are not commonly used in Python.

<br><br><br>

<Blockquote>Four rule calculations</Blockquote>
Python can do four arithmetic operations (+, -, *, /).
{% highlight python %}
>>> a = 1
>>> b = 2
>>> a + b
3
{% endhighlight %}
{% highlight python %}
>>> a * b
2
>>> a / b
0.5
{% endhighlight %}

<br>

<Blockquote>**Operator</Blockquote>
The \*\* operator is used like x\*\*y, which returns the value of x to the power of y.
{% highlight python %}
>>> a = 2
>>> b = 3
>>> a ** b
8
{% endhighlight %}

<br>

<Blockquote>%Operator</Blockquote>
% Is an operator that returns the remainder of division, as you can see if you have used it in c language or c++.
{% highlight python %}
>>> 8 % 3
2
>>> 3 % 8
3
{% endhighlight %}

<br>

<Blockquote>//Operator</Blockquote>
Using only one / returns the entire division quotient.
{% highlight python %}
>>> 9 / 2
4.5
{% endhighlight %}
If two // are used, only integer values are returned after division.
{% highlight python %}
>>> 9 // 2
4
{% endhighlight %}

<br>


---------------------------------------------------------------------------------------------------
</div>
</details>
<br>

숫자형(Number)은 숫자 형태로 이루어진 자료형으로 1, 2, 3과 같은 정수, 3.14와같은 실수, 그리고 8진수나 16진수같은 것들이 있다.<br><br>

|항목|예제|
|:---:|:---:|
|정수|365, -500, 0|
|실수|3.14, -3.14, 2.8e|
|8진수|0o46, 0o25|
|16진수|0xF1, 0x3A|
{:.mbtablestyle}
<br><br>

<Blockquote>정수형</Blockquote>
정수형은 이름 그대로 정수를 뜻하는 자료형이다.
{% highlight python %}
>>> num = 365
>>> num = -500
>>> num = 0
{% endhighlight %}

<br>
<Blockquote>실수형</Blockquote>
파이썬에서 실수형(Floating-point)은 소수점이 포함된 숫자를 말한다.
{% highlight python %}
>>> num = 3.14
>>> num = -3.14
{% endhighlight %}
위와 같은 방식은 우리가 흔히 쓰는 방식인데 컴퓨터가 사용하는 표현은 아래와 같다.
{% highlight python %}
>>> num = 3.14e10
>>> num = 3.14E-10
{% endhighlight %}
e나 E로 표기해도 상관없다.

<br>

<Blockquote>8진수와 16진수</Blockquote>
8진수는 0o로 표기하면된다(0O도 가능하다).
{% highlight python %}
>>> num = 0o12
{% endhighlight %}
16진수는 0x로 표기한다.
{% highlight python %}
>>> num = 0xFF
>>> num = 0x1A
{% endhighlight %}
8진수나 16진수는 파이썬에서 잘 사용하지 않는 형태의 숫자 자료형이다.

<br><br><br>

<Blockquote>사칙연산</Blockquote>
파이썬으로 사칙연산(+, -, *, /)를 할 수 있다.
{% highlight python %}
>>> a = 1
>>> b = 2
>>> a + b
3
{% endhighlight %}
{% highlight python %}
>>> a * b
2
>>> a / b
0.5
{% endhighlight %}

<br>

<Blockquote>**연산자</Blockquote>
\*\*연산자는 x\*\*y처럼 사용하는데, x의 y제곱값을 반환한다.
{% highlight python %}
>>> a = 2
>>> b = 3
>>> a ** b
8
{% endhighlight %}

<br>

<Blockquote>%연산자</Blockquote>
%는 c언어나 c++에서 사용해봤다면 알 수 있듯이 나눗셈의 나머지 값을 돌려주는 연산자이다.
{% highlight python %}
>>> 8 % 3
2
>>> 3 % 8
3
{% endhighlight %}

<br>

<Blockquote>//연산자</Blockquote>
/를 하나만 사용하면 나눗셈의 몫 전체를 반환해준다.
{% highlight python %}
>>> 9 / 2
4.5
{% endhighlight %}
//를 두개사용하면 나눗셈한 후 정수값만 반환해준다.
{% highlight python %}
>>> 9 // 2
4
{% endhighlight %}