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

String function
=====

The string data type has its own function. To use it, add '.' after the string variable and use the name of the function to be used.<br>
<br>

<Blockquote>Counting the number of characters(count)</Blockquote>
{% highlight python %}
>>> string = "Hello"
>>> string.count("l")
2
{% endhighlight %}
The count in the example above returns the number of characters 'l' to find.<br><br>

<Blockquote>Print the location(find)</Blockquote>
{% highlight python %}
>>> string = "Hello World"
>>> string.find('r')
8
>>> string.find('a')
-1
{% endhighlight %}
In the above example, if 'r' is found, the position of the first occurrence of 'r' is returned. However, if a missing character is entered, -1 is returned.<br><br>

<Blockquote>Print the location(index)</Blockquote>
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
The example index above returns the position of the first character, like find. However, if you enter a missing character, an error occurs.<br><br>


<Blockquote>Insert string(join)</Blockquote>
{% highlight python %}
>>> ",".join("1234")
'1,2,3,4'
{% endhighlight %}
The join function inserts a ',' between each of the 1234 strings. The join function can use not only strings but also lists and tuples as input.<br>
How to use it as a list is as follows.

{% highlight python %}
>>> ",".join(['1','2','3','4'])
'1,2,3,4'
{% endhighlight %}
<br>

<Blockquote>Change lowercase to uppercase(upper)</Blockquote>
{% highlight python %}
>>> string = "hello"
>>> string.upper()
'HELLO'
{% endhighlight %}
It literally converts lowercase letters to uppercase letters. However, if it is already in capital letters, there is no change.<br><br>

<Blockquote>Change uppercase to lowercase(lower)</Blockquote>
{% highlight python %}
>>> string = "HELLO"
>>> string.lower()
'hello'
{% endhighlight %}
This also literally converts uppercase letters to lowercase letters. But if it's already in lowercase, nothing changes.<br><br>

<Blockquote>Erase left space(lstrip)</Blockquote>
{% highlight python %}
>>> string = "    Hello    "
>>> string.lstrip()
'Hello    '
{% endhighlight %}
lstrip is a function that removes one or more consecutive whitespaces from the leftmost of a string. In lstrip, 'l' means left.<br><br>

<Blockquote>Erase right space(rstrip)</Blockquote>
{% highlight python %}
>>> string = "    Hello    "
>>> string.rstrip()
'    Hello'
{% endhighlight %}
rstrip is a function that removes one or more consecutive spaces from the rightmost space of a string. In rstrip, 'r' means right.<br><br>

<Blockquote>Erase both spaces(strip)</Blockquote>
{% highlight python %}
>>> string.strip()
'Hello'
{% endhighlight %}
strip is a function that removes all spaces from one or more consecutive spaces on either side of a string.<br><br>

<Blockquote>Replace string(replace)</Blockquote>
{% highlight python %}
>>> string = "Hello World"
>>> string.replace("World", "People")
'Hello People'
{% endhighlight %}
This function is used like replace (the string to be replaced, the string to replace) to replace a specific value in a string with another value.<br><br>

<Blockquote>Splitting a string(split)</Blockquote>
{% highlight python %}
>>> string = "I like number 7"
>>> string.split()
['I', 'like', 'number', '7']
{% endhighlight %}
As above, if nothing is put in the parentheses of the split, the string is divided based on space (space, tab, enter, etc.).

{% highlight python %}
>>> number = "1:2:3:4"
>>> number.split(':')
['1', '2', '3', '4']
{% endhighlight %}
However, if a specific character is put in parentheses as above, it is divided based on the specific character.<br><br>

<Blockquote>Finding the length of a string(len)</Blockquote>
{% highlight python %}
>>> string = "Hello World"
>>> len(string)
11
{% endhighlight %}
If you put the variable name in parentheses, it tells you the length of the string.



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
위의 예제 count는 찾고자 하는 문자 'l'의 개수를 반환해준다.<br><br>

<Blockquote>위치 알려주기(find)</Blockquote>
{% highlight python %}
>>> string = "Hello World"
>>> string.find('r')
8
>>> string.find('a')
-1
{% endhighlight %}
위의 예제 find는 'r'을 찾으면 'r'이 처음나온 위치를 반환해준다. 하지만 없는 문자를 넣는다면 -1을 반환해준다.<br><br>

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
위의 예제 index는 find와 같이 처음나온 문자의 위치를 반환해준다. 하지만 없는 문자를 넣으면 오류가 발생한다.<br><br>


<Blockquote>문자열 삽입(join)</Blockquote>
{% highlight python %}
>>> ",".join("1234")
'1,2,3,4'
{% endhighlight %}
위의 예제 join함수는 1234문자열의 각각의 사이에 ','를 삽입한다. join함수는 문자열뿐만 아니라 리스트나 튜플도 입력으로 사용할 수 있다.<br>
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
위와같이 split의 괄호안에 아무것도 넣지않으면 공백(스페이스, 탭, 엔터 등)을 기준으로 문자열을 나누어준다.

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
