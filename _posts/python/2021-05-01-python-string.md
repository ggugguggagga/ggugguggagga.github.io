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

String
=====
<br>
Strings literally refer to characters. It can be a simple word like "Hello", a single letter like "A", "B", or a number is also called a string.
{% highlight python %}
"Hello World"
"A"
"365"
{% endhighlight %}
If you look at the example code above, you can see that the string is marked with double quotation marks ("), but in Python, there are a total of 4 ways to express it.<br><br><br>

Typically, there are double quotation marks (") and single quotation marks (') as we know them, but you can use double quotation marks (""") or single quotation marks (''') three times in a row. However, it is common to just use double quotes (") or single quotes (').
{% highlight python %}
"Hello World"
'Hello World'
"""Hello World"""
'''Hello World'''
{% endhighlight %}

-----

If you want to put single or double quotes inside a string, you can use three methods.
<br>
<Blockquote>Using single quotes</Blockquote>
{% highlight python %}
>>> string = "I'm programmer"
>>> string
"I'm programmer"
{% endhighlight %}
If you want to use single quotes, just enclose the string to be used in double quotes. In this way, single quotes inside double quotes are recognized as characters, so you can just use them.
<Blockquote>Using double quotes</Blockquote>
{% highlight python %}
>>> string = '"Hello" I say'
>>> string
'"Hello" I say'
{% endhighlight %}
Contrary to the above, if you wrap a string with single quotation marks, double quotation marks can be used because double quotation marks are recognized as characters.
{% highlight python %}
>>> string = 'I'm programmer'
SyntaxError: invalid syntax
{% endhighlight %}
Note that, for example, if you put single quotes inside single quotes, it is a SyntaxError, so be careful.
{% highlight python %}
>>> "I"m programmer"
SyntaxError: invalid syntax
{% endhighlight %}
The double quotes above are grammatically nonsense, but they are used to show examples. If you use double quotes when they are enclosed in double-quotes, a SyntaxError will occur, so be careful.
<Blockquote>백슬래시(\\)</Blockquote>
{% highlight python %}
>>> intro = 'I\'m programmer'
>>> string = "\"Hello\" I say"
{% endhighlight %}
It is usually used in Markdown or HTML, or in C or C++. That's the backslash. If so, you can use the character we want to use even if it is enclosed in double or single quotes. It will be easier to understand by looking at the example above.

------

When using strings, there are times when you want to change paragraphs, and there are a total of three ways to do this.<br><br>

<Blockquote>\n</Blockquote>
{% highlight python %}
>>> string = "Hello\n World"
{% endhighlight %}
Like this, you can use \n, which is also used in c or c++, to space lines. However, it has the disadvantage of poor readability and lengthening.

<Blockquote>3 single quotes('''), 3 double quotation marks(""")</Blockquote>
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
If you use the 3 double quotation marks (""") and 3 single quotation marks ("') used to represent the character above, you can conveniently use it when changing paragraphs. First, use 3 single or double quotation marks and write them down. If you want to change the paragraph after writing down the words you want to change, press Enter and confirm. You can see that the paragraph has changed.


----------


Escape code
=====
<br>

|Code|Explanation|
|:---:|:---:|
|\n|When changing a line in a string|
|\t|When giving tab space between strings|
|\\\\ |When printing the character \\ |
|\\\'|When printing single quotation marks (')|
|\\\"|When printing double quotation marks (")|
|\r|Carriage return (line feed character, moves the current cursor to the front)|
|\f|Form Pit (newline character, moves the current cursor to the next line)|
|\a|Bell sound (the PC speaker makes a "beep" sound when output)|
|\b|Backspace|
|\000|Null character|
{:.mbtablestyle}




-----------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------
</div>
</details>
<br>

문자열
=====
<br>
문자열은 말그대로 문자들을 말하는 것이다. 간단하게 "안녕하세요", "Hello"와 같은 단어도 되고, "A", "B"와 같은 한 개의 문자나 아니면 숫자도 문자열이라고 한다.
{% highlight python %}
"Hello World"
"A"
"365"
{% endhighlight %}
위의 예제 코드를 보면 큰따옴표(")로 문자열을 표시한것을 볼 수 있지만 파이썬에서는 표현할 수 있는 방법이 총 4가지가 된다.<br><br><br>

대표적으로 우리가 알고있는 큰 따옴표(")와 작은 따옴표(')가 있지만 큰 따옴표(""")를 사용하거나 작은 따옴표(''')를 연속으로 세 번씩 적어서 사용할 수 있다. 하지만 보통 그냥 큰 따옴표(")나 작은 따옴표(')를 쓰는게 일반적이다.
{% highlight python %}
"Hello World"
'Hello World'
"""Hello World"""
'''Hello World'''
{% endhighlight %}

-----

만약 문자열 안에 작은 따옴표나 큰 따옴표를 넣고싶다면 세 가지 방법을 사용할 수 있다.
<br>
<Blockquote>작은따옴표 사용하기</Blockquote>
{% highlight python %}
>>> string = "I'm programmer"
>>> string
"I'm programmer"
{% endhighlight %}
작은 따옴표를 사용하고 싶다면 사용할 문자열을 큰 따옴표로 감싸면 된다. 이렇게 사용하면 큰 따옴표 안에 있는 작은 따옴표는 그냥 문자로 인식하기 때문에 그냥 사용할 수 있다.
<Blockquote>큰따옴표 사용하기</Blockquote>
{% highlight python %}
>>> string = '"Hello" I say'
>>> string
'"Hello" I say'
{% endhighlight %}
큰 따옴표를 사용하고 싶으면 위와 반대로 작은 따옴표로 문자열을 감싸면 큰 따옴표를 문자로 인식하기때문에 큰 따옴표를 사용할 수 있다.
{% highlight python %}
>>> string = 'I'm programmer'
SyntaxError: invalid syntax
{% endhighlight %}
여기서 주의할 점은 예를 들어 작은 따옴표로 감싼곳안에 작은 따옴표를 넣으면 이는 SyntaxError이므로 주의해야한다.
{% highlight python %}
>>> "I"m programmer"
SyntaxError: invalid syntax
{% endhighlight %}
위에 큰 따옴표는 문법적으로 말이 안되지만 예시를 보여주기위해 사용한 것으로 큰 따옴표 또한 큰 따옴표에 감싸져있을 때 사용하면 SyntaxError가 발생하므로 주의해야한다.
<Blockquote>백슬래시(\\)</Blockquote>
{% highlight python %}
>>> intro = 'I\'m programmer'
>>> string = "\"Hello\" I say"
{% endhighlight %}
보통 마크다운이나 HTML에서 사용하거나 C언어, c++에서 사용하는 방법이다. 바로 백슬래시를 사용하는 것이다. 그렇다면 큰 따옴표에 감싸져있거나 작은 따옴표에 감싸져있다해도 우리가 사용하고 싶은 문자를 사용할 수 있다. 위의 예제를 보면 이해가 쉽게 될 것이다.

------

문자열을 사용하다보면 줄을 띄우고 싶을 때가 있는데 이는 총 3가지 방법이 있다.<br><br>

<Blockquote>\n</Blockquote>
{% highlight python %}
>>> string = "Hello\n World"
{% endhighlight %}
이렇게 c나 c++에서도 사용되는 \n를 사용해서 줄의 띄울 수 있다. 하지만 가독성이 떨어지고 길어지는 단점을 가지고있다.

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
위에서 문자를 나탈 때 사용하던 큰 따옴표(""") 3개와 작은 따옴표(''') 3개를 사용하면 줄을 띄울 때 편리하게 사용할 수 있다. 먼저 작은 따옴표나 큰 따옴표를 3개사용하고 적고싶은 말을 적고나서 띄우고 싶으면 엔터를 쳐서 띄우고 변수에 넣어서 확인하면 잘 띄어져있는 것을 확인할 수 있다.


----------


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

