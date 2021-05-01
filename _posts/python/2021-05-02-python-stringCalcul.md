---
layout: post
title: 파이썬 문자열 연산[Python String operation]
image: python.jpg
date: 2021-05-02-01:09
tags: [python, string_Calculate]
categories: python
---

<details>
<summary>English</summary>
<div markdown="1">

String operation
=====

<br>
In Python, you can do string operations. If you've ever tried C or C++, you did add certain words together maybe. However, in Python, it is also possible to multiply.
<br>
<Blockquote>addition</Blockquote>
{% highlight python %}
>>> first = "Hello"
>>> second = " World"
>>> first + second
'Hello World'
{% endhighlight %}
Looking at the top, you can see the output of "Hello" and "world" combined with +.

<Blockquote>multiplication</Blockquote>
{% highlight python %}
>>> string = "Hello"
>>> string * 2
'HelloHello'
{% endhighlight %}
Multiplication literally simply multiplies by a certain number and outputs a string.

{% highlight python %}
>>> string = "3.14 Hello World"
>>> string * 2
'3.14 Hello World3.14 Hello World'
{% endhighlight %}
You can see that the output is good even if you combine several words as above.

{% highlight python %}
>>> string * 1.2
Traceback (most recent call last):
  File "<pyshell#2>", line 1, in <module>
    string * 1.2
TypeError: can't multiply sequence by non-int of type 'float'
{% endhighlight %}
However, you can see that a TypeError occurs when multiplying a decimal number rather than an integer.
<br>
So, what do you use multiplication? Of course, it can be very useful when you want to print a string multiple times. However, it can also be useful when displaying information neatly.

{% highlight python %}
string = '''date: 2021-05-02
project: String operation'''
print("-" * 15)
print(string)
print("-" * 15)
{% endhighlight %}
If you use it as above, you can clearly see it in the console when running the project.
{% highlight python %}
---------------
data: 2021-05-02     
project: String operation
--------------- 
{% endhighlight %}




-----------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------
</div>
</details>


문자열 연산
=====

<br>
파이썬에서는 문자열 연산을 할 수 있다. C나 C++를 해봤다면 흔하게 특정 단어들을 더해서 합해 봤을 것이다. 하지만 파이썬에서는 곱하기도 가능하다.
<br>
<Blockquote>더하기</Blockquote>
{% highlight python %}
>>> first = "Hello"
>>> second = " World"
>>> first + second
'Hello World'
{% endhighlight %}
위를 보면 "Hello"와 "world"를 +를 이용해 합해서 출력한 것을 볼 수 있다.

<Blockquote>곱하기</Blockquote>
{% highlight python %}
>>> string = "Hello"
>>> string * 2
'HelloHello'
{% endhighlight %}
곱하기는 말 그대로 그냥 특정 수 만큼 곱해서 문자열을 출력해준다.

{% highlight python %}
>>> string = "3.14 Hello World"
>>> string * 2
'3.14 Hello World3.14 Hello World'
{% endhighlight %}
위와같이 여러단어를 합한것도 출력이 잘되는 것을 볼 수 있다.

{% highlight python %}
>>> string * 1.2
Traceback (most recent call last):
  File "<pyshell#2>", line 1, in <module>
    string * 1.2
TypeError: can't multiply sequence by non-int of type 'float'
{% endhighlight %}
하지만 정수가 아닌 소수를 곱하면 TypeError가 발생하는것을 볼 수 있다.
<br>
그렇다면 곱하기는 어디에 사용하는가? 물론 문자열을 여러번 출력하고 싶을 때 아주 유용하게 사용할 수 있다. 하지만 뭔가 정보를 깔끔하게 보여줄 때도 유용하게 사용할 수 있다.

{% highlight python %}
string = '''날짜: 2021-05-02
프로젝트: 문자열 연산'''
print("-" * 15)
print(string)
print("-" * 15)
{% endhighlight %}
위와같이 사용한다면 프로젝트를 실행할 때 콘솔에서 확실하게 눈에 들어오게 사용할 수 있다.
{% highlight python %}
---------------
날짜: 2021-05-02     
프로젝트: 문자열 연산
--------------- 
{% endhighlight %}

