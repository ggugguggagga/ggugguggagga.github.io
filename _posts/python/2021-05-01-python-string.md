---
layout: post
title: 파이썬 자료형(문자열)[Python String]
image: python.jpg
date: 2021-05-01-18:10
tags: [python, string]
categories: python
---

<details>
<summary>English</summary>
<div markdown="1">


-----------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
</div>
</details>
<br>

문자열
=====
<br>
문자열(String)이란 문자나 단어등으로 구성된 문자들의 집합을 의미한다.
{% highlight python %}
"Hello World"
"A"
"365"
{% endhighlight %}
위와 같은 예시를 보면 큰따옴표(")를 사용해서 문자열을 만들 수 있지만 파이썬에서 문자열을 사용하는 방법은 총 4가지이다.<br><br><br>


<Blockquote>큰 따옴표(")</Blockquote>
{% highlight python %}
"Hello World"
{% endhighlight %}

<Blockquote>작은 따옴표(')</Blockquote>
{% highlight python %}
'Hello World'
{% endhighlight %}

<Blockquote>큰따옴표 3개(""")</Blockquote>
{% highlight python %}
"""Hello World"""
{% endhighlight %}

<Blockquote>작은따옴표 3개(''')</Blockquote>
{% highlight python %}
'''Hello World'''
{% endhighlight %}
<br>

-----

<br>
<Blockquote>작은따옴표 사용하기</Blockquote>
{% highlight python %}
>>> string = "I'm programmer"
>>> string
"I'm programmer"
{% endhighlight %}
위와같이 문자열을 큰 따옴표(")에 둘러싸이게하면 큰 따옴표 안에 들어있는 작은 따옴표는 기호로 인식되지 않기때문에 일반 문자처럼 사용할 수 있다.<br>
<br>
여기서 만약 큰 따옴표(")가 아닌 작은 따옴표(')를 사용한다면 SyntaxError가 발생한다.
{% highlight python %}
>>> string = 'I'm programmer'
SyntaxError: invalid syntax
{% endhighlight %}
<Blockquote>큰따옴표 사용하기</Blockquote>
{% highlight python %}
>>> string = '"Hello" I say'
>>> string
'"Hello" I say'
{% endhighlight %}
위와같이 작은 따옴표(')를 사용하면 큰 따옴표(")를 일반 문자처럼 사용할 수 있다. 즉, 작은따옴표(')안에 사용된 큰 따옴표는(")문자열을 만드는 기호로 인식되지않는다.
<Blockquote>백슬래시(\\)</Blockquote>
{% highlight python %}
>>> intro = 'I\'m programmer'
>>> string = "\"Hello\" I say"
{% endhighlight %}
위와같이 백슬래시(\\)를 사용하면 백슬래쉬 뒤에오는 문자는 기호의 의미가 아니라 문자 자체를 사용하게된다.
<br>

------

<br>
여러 줄로 나뉜 문자열을 변수에 대입하고 싶을 때는 크게 두 가지 방법이 있다.<br><br>

<Blockquote>\\n</Blockquote>
{% highlight python %}
>>> string = "Hello\n World"
{% endhighlight %}
위와같이 줄바꿈 문자인 '\\n'을 사용하는 방법이 있지만 한눈에 알아보기 힘들고 줄이 길어지는 단점이 있다.

<Blockquote>작은따옴표 3개('''), 큰따옴표 3개(""")</Blockquote>
{% highlight python %}
>>> string = '''Hello
World'''
>>> print(string)
Hello
World
{% endhighlight %}

{% highlight python %}
>>> string = """Hello
World"""
>>> print(string)
Hello
World
{% endhighlight %}
위와같이 문자열이 길고 여러줄인 경우는 '\\n'보다는 위와같은 방법을 사용하는 것이 좋다.

<br>

----------

<br>

이스케이프 코드
=====
<br>

|코드|설명|
|:---:|:---:|
|\n|문자열 안에서 줄을 바꿀 때|
|\t|문자열 사이에 탭 간격을 줄 때|
|\\\\ |문자 \\를 출력할 때|
|\\\'|작은 따옴표(')를 출력할 때|
|\\\"|큰 따옴표(")를 출력할 때|
|\r|캐리지 리턴(줄 바꿈 문자, 현재 커서를 가장 앞으로 이동)|
|\f|폼 피트(줄 바꿈 문자, 현재 커서를 다음 줄로 이동)|
|\a|벨 소리(출력할 때 PC스피커에서 "삑"소리가 난다)|
|\b|백스페이스|
|\000|널 문자|
{:.mbtablestyle}

<br>

--------------------

<br>

문자열 연산
=====

<br>
파이썬에서는 문자열을 더하거나 곱할 수 있다. 문자열을 더하는건 연결하는 역할을 하고, 곱하기는 곱한 수만큼 그 문자열이 나오게 할 수 있다.
<br>
<Blockquote>더하기</Blockquote>
{% highlight python %}
>>> first = "Hello"
>>> second = " World"
>>> first + second
'Hello World'
{% endhighlight %}
위의 코드는 보이는 그대로 first다음에 second를 붙인 것이다.

<Blockquote>곱하기</Blockquote>
{% highlight python %}
>>> string = "Hello"
>>> string * 2
'HelloHello'
{% endhighlight %}

<Blockquote>곱하기 응용</Blockquote>
곱하기를 사용하기 좋은 경우는 구간을 나눠서 깔끔하게 보이도록 할 때 사용하면 좋다.
{% highlight python %}
print("-" * 30)
print("Hello World")
print("-" * 30)
{% endhighlight %}

위와같이 사용할 경우 아래와 같이 출력된다.
{% highlight python %}
------------------------------
Hello World
------------------------------
{% endhighlight %}

<Blockquote>문자열 길이 구하기</Blockquote>
파이썬에서 len 함수를 사용하면 문자열의 길이를 알 수 있다.
{% highlight python %}
>>> string = "Hello World"
>>> len(string)
11
{% endhighlight %}
<br>

-----------------------------

<br>

문자열 인덱싱과 슬라이싱
=====

<Blockquote>인덱싱</Blockquote>
{% highlight python %}
>>> string = "Hello World"
{% endhighlight %}
위 문자열에 번호를 매기면 아래와 같다.


|H|e|l|l|o||W|o|r|l|d|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|0|1|2|3|4|5|6|7|8|9|10|
{:.mbtablestyle}


파이썬은 0부터 숫자를 센다.
{% highlight python %}
>>> string = "Hello World"
>>> string[4]
'o'
{% endhighlight %}