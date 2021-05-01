---
layout: post
title: 파이썬 문자열 함수[Python String Function]
image: python.jpg
date: 2021-05-02-02:30
tags: [python, string_function]
categories: python
---

<details>
<summary>English</summary>
<div markdown="1">





-----------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------
</div>
</details>

문자열 함수
=====

문자열 자료형은 자체적인 함수를 가졌는데 이를 사용할려면 문자열 변수 뒤에 '.'를 붙이고 사용할 함수의 이름을 써주면된다.<br>
<br>

<Blockquote>문자 개수 세기(count)</Blockquote>
{% highlight python %}
>>> string = "Hello"
>>> string.count("l")
2
{% endhighlight %}
count는 찾고자 하는 문자 'l'의 개수를 반환해준다.<br><br>

<Blockquote>위치 알려주기(find)</Blockquote>
{% highlight python %}
>>> string = "Hello World"
>>> string.find('r')
8
>>> string.find('a')
-1
{% endhighlight %}
'r'을 찾으면 'r'이 처음나온 위치를 반환해준다. 하지만 없는 문자를 넣는다면 -1을 반환해준다.<br><br>

<Blockquote>위치 알려주기(index)</Blockquote>
{% highlight python %}
>>> string = "Hello World"
>>> string.index('W')
6
>>> string.index('w')
Traceback (most recent call last):
  File "<pyshell#18>", line 1, in <module>
    string.index('w')
ValueError: substring not found
{% endhighlight %}
index는 find와 같이 처음나온 문자의 위치를 반환해준다. 하지만 없는 문자를 넣으면 오류가 발생한다.<br><br>


<Blockquote>문자열 삽입(join)</Blockquote>
{% highlight python %}
>>> ",".join("1234")
'1,2,3,4'
{% endhighlight %}
join함수는 1234문자열의 각각의 사이에 ','를 삽입한다. join함수는 문자열뿐만 아니라 리스트나 튜플도 입력으로 사용할 수 있다.<br>
리스트로 사용하는 방법은 아래와 같다.

{% highlight python %}
>>> ",".join(['1','2','3','4'])
'1,2,3,4'
{% endhighlight %}
<br>

<Blockquote>소문자를 대문자로 바꾸기(upper)</Blockquote>
{% highlight python %}
>>> string = "hello"
>>> string.upper()
'HELLO'
{% endhighlight %}
말그대로 소문자를 대문자로 바꿔준다. 하지만 이미 대문자라면 변화가 없다.<br><br>

<Blockquote>대문자를 소문자로 바꾸기(lower)</Blockquote>
{% highlight python %}
>>> string = "HELLO"
>>> string.lower()
'hello'
{% endhighlight %}
이것또한 말그대로 대문자를 소문자로 바꿔준다. 하지만 이미 소문자라면 아무런 변화가 없다.<br><br>

<Blockquote>왼쪽 공백 지우기(lstrip)</Blockquote>
{% highlight python %}
>>> string = "    Hello    "
>>> string.lstrip()
'Hello    '
{% endhighlight %}
lstrip은 문자열 중 가장 왼쪽에 있는 한 칸이상의 연속된 공백들을 지우는 함수이다. lstrip에서 'l'은 left를 의미한다.<br><br>

<Blockquote>오른쪽 공백 지우기(rstrip)</Blockquote>
{% highlight python %}
>>> string = "    Hello    "
>>> string.rstrip()
'    Hello'
{% endhighlight %}
rstrip은 문자열 중 가장 오른쪽에 있는 한 칸이상의 연속된 공백들을 지우는 함수이다. rstrip에서 'r'은 right를 의미한다.<br><br>

<Blockquote>양쪽 공백 지우기(strip)</Blockquote>
{% highlight python %}
>>> string.strip()
'Hello'
{% endhighlight %}
strip은 문자열 양쪽에 있는 한 칸 이상의 연속된 공백을 모두 지우는 함수이다.<br><br>

<Blockquote>문자열 바꾸기(replace)</Blockquote>
{% highlight python %}
>>> string = "Hello World"
>>> string.replace("World", "People")
'Hello People'
{% endhighlight %}
replace(바뀌게 될 문자열, 바꿀 문자열)처럼 사용해 문자열 안의 특정 값을 다른 값으로 바꿔주는 함수이다.<br><br>

<Blockquote>문자열 나누기(split)</Blockquote>
{% highlight python %}
>>> string = "I like number 7"
>>> string.split()
['I', 'like', 'number', '7']
{% endhighlight %}
위와같이 spllit의 괄호안에 아무것도 넣지않으면 공백(스페이스, 탭, 엔터 등)을 기준으로 문자열을 나누어준다.

{% highlight python %}
>>> number = "1:2:3:4"
>>> number.split(':')
['1', '2', '3', '4']
{% endhighlight %}
하지만 위와 같이 괄호안에 특정 문자를 넣으면 특정 문자를 기준으로 나누어준다.<br><br>

<Blockquote>문자열 길이 구하기(len)</Blockquote>
{% highlight python %}
>>> string = "Hello World"
>>> len(string)
11
{% endhighlight %}
괄호안에 변수이름을 넣으면 문자열길이를 알려준다.
