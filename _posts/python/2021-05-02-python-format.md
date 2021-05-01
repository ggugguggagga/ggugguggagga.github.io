---
layout: post
title: 파이썬 포매팅[Python Format]
image: python.jpg
date: 2021-05-02-01:44
tags: [python, Format]
categories: python
---

<details>
<summary>English</summary>
<div markdown="1">

Format
=====

If I wrote a program that tells today's date, if today's date is 2021-05-02, the following will be displayed.
{% highlight python %}
2021년 5월 2일

//년 == year
//월 == month
//일 == day
{% endhighlight %}
Then, when tomorrow comes, it will be the 3rd, not the 2nd, and if the next month comes, it will be June instead of May, and the year will also be 2022. Here, there are cases where the values of the year, month, and day do not change, but only numbers need to be changed.<br>
<br>
Of course, in format, not only numbers are possible, but numbers, letters, and variables can be entered.


|Code|Explanation|
|:---:|:---:|
|\s|String|
|\c|Character|
|\d|Integer|
|\f|Floating-point|
|\o|Octal|
|\x|Hexadecimal|
|%%|Literal %|
{:.mbtablestyle}


If you have using the c language, you will be familiar with some of the tables above.

<Blockquote>Number</Blockquote>
{% highlight python %}
>>> "I like number %d" %7
'I like number 7'
{% endhighlight %}
%d is an integer as shown in the table above.<br><br>

<Blockquote>String</Blockquote>
{% highlight python %}
>>> "I like nuber %s" %"one"
'I like nuber one'
{% endhighlight %}
%s can be assigned a string.<br><br>

<Blockquote>Variable name</Blockquote>
{% highlight python %}
>>> number = 5
>>> "I like number %d" %number
'I like number 5'
{% endhighlight %}
It is also possible to specify a variable and put it in.<br><br>

<Blockquote>2 values</Blockquote>
{% highlight python %}
>>> number = 7
>>> string = "seven"
>>> "I like number %d (%s)" %(number, string)
'I like number 7 (seven)'
{% endhighlight %}
If you want to put two values, you can write the code using comma (,) as in the example above in turn.<br><br>

<Blockquote>Alignment, blank</Blockquote>
You can also use %d and %s as follows.
{% highlight python %}
>>> "%10s" %"Hello"
'     Hello'
{% endhighlight %}
Since the above code creates 10 digits and puts 'Hello' at the end, you can right-justify 'Hello' on the right and leave the rest of the digits blank.<br><br>

{% highlight python %}
>>> "%-10sWorld" %"Hello"
'Hello     World'
{% endhighlight %}
Then, in Python, minus can be used, so you can use minus when left aligning and 'Hello' to see left-aligned Hello. Also, if you put a word after %-10s, you first make 10 digits, then put 'Hello' and fill in the blanks, and then put 'World'. If you look at the code above, you can see that there are 10 digits before 'World'.<br><br>

<Blockquote>decimal point</Blockquote>
{% highlight python %}
>>> "%0.5f" %3.14159265358979323846264338327950288
'3.14159'
{% endhighlight %}
If you do not want to display all the decimal points and want to indicate to which digit, you can print to the desired digit by inserting.[the number of digits you want] and adding f for float.<br><br>

<Blockquote>format</Blockquote>
You can format as above, but there is a format function in Python, which allows you to format conveniently.<br>
<br>

**Number**
{% highlight python %}
>>> "I like number {0}" .format(7)
'I like number 7'
{% endhighlight %}
<br>

**String**
{% highlight python %}
>>> "I like number {0}" .format("one")
'I like number one'
{% endhighlight %}
<br>

**2 or more values**
{% highlight python %}
>>> number = 7
>>> string = seven
>>> "I like number {0} ({1})" .format(number, string)
'I like number 7 (seven)'
{% endhighlight %}
If two or more values are entered, the values are entered sequentially by entering them in the order of {0} and {1}.<br><br>

**Variable name**
{% highlight python %}
>>> "I like number {number} ({string})" .format(number = 7, string = "seven")
'I like number 7 (seven)'
{% endhighlight %}
You can also set a value by setting a variable.<br><br>

**Left align**
{% highlight python %}
>>> "{0:<10}".format("Hello")
'Hello     '
{% endhighlight %}
The format function can also be left justified.<br><br>

**Right aligned**
{% highlight python %}
>>> "{0:>10}".format("Hello")
'     Hello'
{% endhighlight %}
If you use <for left alignment, and use> for right alignment, you can see that it is right-aligned.<br><br>

**Fill in the blanks**
{% highlight python %}
>>> "{0:~^10}".format("Hello")
'~~Hello~~~'
>>> "{0:!<10}".format("Hello")
'Hello!!!!!'
{% endhighlight %}
Spaces can be filled in by inserting the desired character before using one of <, >, and ^ and using alignment.<br><br>

**Representing the decimal point**
{% highlight python %}
>>> radi = 3.14159265358979323846264338327950288
>>> "{0:0.3f}".format(radi)
'3.142'
{% endhighlight %}
As with the decimal point above, you can use f to print to the desired digit.<br><br>

{% highlight python %}
>>> radi = 3.14159265358979323846264338327950288
>>> "{0:10.3f}".format(radi)
'     3.142'
{% endhighlight %}
Of course, you can also make 10 digits as above.<br><br>

**{ }**
{% highlight python %}
>>> "{{  }}".format()
'{  }'
{% endhighlight %}
If you want to use brace characters like {} literally, not formatting characters, you can use {{ }} two consecutively like this.<br><br>

<Blockquote>f 문자열 포매팅</Blockquote>
{% highlight python %}
>>> number = 7
>>> string = "seven"
>>> f"I like {number} ({string})"
'I like 7 (seven)'
{% endhighlight %}
From Python 3.6 or higher, the f string format can be used. It cannot be used in versions below it. As above, you can use the string format function by prefixing the string with the f prefix. Anything after f can be either double quotes or single quotes.<br><br>

{% highlight python %}
>>> number = 7
>>> f'I like number {number + 1}'
'I like number 8'
{% endhighlight %}
It is also possible to output by adding values as above.<br><br>

{% highlight python %}
>>> d = {'string' : 'one', 'number' : 1}
>>> f'I like {d["number"]} ({d["string"]})'
'I like 1 (one)'
{% endhighlight %}
\[ \] is used as above in f string formatting.<br><br>

{% highlight python %}
>>> f'{"Hello":<10}'
'Hello     '
>>> f'{"Hello":>10}'
'     Hello'
>>> f'{"Hello":^10}'
'  Hello   '
>>> 
{% endhighlight %}
Alignment is used as above.<br><br>

{% highlight python %}
>>> f'{"Hello":-^10}'
'--Hello---'
>>> f'{"Hello":~<10}'
'Hello~~~~~'
{% endhighlight %}
Spaces are also used as above.<br><br>

{% highlight python %}
>>> f'{radi:0.3f}'
'3.142'
>>> f'{radi:10.3f}'
'     3.142'
{% endhighlight %}
Decimal points with decimal points and spaces are used as above.<br><br>

{% highlight python %}
>>> f'{{  }}'
'{  }'
{% endhighlight %}
If you want to use {} characters, you can use both at the same time as above.

-----------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------
</div>
</details>

포매팅
=====

만약 내가 오늘 날짜를 알려주는 프로그램을 작성했다고 할 때 오늘 날짜가 2021-05-02라면 아래와 같이 출력할 것이다.
{% highlight python %}
2021년 5월 2일
{% endhighlight %}
그럼 내일이 되었을 때는 2일이 아닌 3일이고 다음달이 된다면 5월이 아닌 6월이 되겠고 년또한 2022년이 될것이다. 여기서 년, 월, 일은 값이 변하지 않고 숫자만 바꿔야하는 경우가 있는데 이를 바꿀 수 있게 하는것이 포매팅이다.<br>
<br>
물론 포매팅에서도 숫자만 가능한것이 아니라 숫자, 문자, 변수를 넣는것이 가능하다.


|코드|설명|
|:---:|:---:|
|\s|문자열(String)|
|\c|문자 1개(Character)|
|\d|정수(Integer)|
|\f|부동 소수(Floating-point)|
|\o|8진수|
|\x|16진수|
|%%|Literal % (문자 '%')|
{:.mbtablestyle}


c언어를 했다면 위의 표중 몇가지는 익숙할 것이다.

<Blockquote>숫자 대입</Blockquote>
{% highlight python %}
>>> "I like number %d" %7
'I like number 7'
{% endhighlight %}
%d는 위에 표에서 본 것과 같이 정수를 넣을 수 있다.<br><br>

<Blockquote>문자열 대입</Blockquote>
{% highlight python %}
>>> "I like nuber %s" %"one"
'I like nuber one'
{% endhighlight %}
%s는 문자열을 대입할 수 있다.<br><br>

<Blockquote>변수명</Blockquote>
{% highlight python %}
>>> number = 5
>>> "I like number %d" %number
'I like number 5'
{% endhighlight %}
변수를 지정해서 넣는 것도 가능하다.<br><br>

<Blockquote>값 2개</Blockquote>
{% highlight python %}
>>> number = 7
>>> string = "seven"
>>> "I like number %d (%s)" %(number, string)
'I like number 7 (seven)'
{% endhighlight %}
만약 값을 두개 넣고 싶다면 차례로 위의 예제처럼 콤마(,)를 이용해서 코드를 작성하면된다.<br><br>

<Blockquote>정렬, 공백</Blockquote>
%d와 %s을 이용해서 아래와 같이 사용할 수도있다.
{% highlight python %}
>>> "%10s" %"Hello"
'     Hello'
{% endhighlight %}
위의 코드는 일단 10개의 자리를 만들고 뒤에 Hello를 넣는것이기 때문에 오른쪽에 Hello를 오른쪽 정렬한 뒤 나머지 자리를 공백으로 남겨둘 수 있다.<br><br>

{% highlight python %}
>>> "%-10sWorld" %"Hello"
'Hello     World'
{% endhighlight %}
그럼 파이썬에서는 마이너스를 사용할 수 있으니 왼쪽정렬을 할때는 마이너스를 사용하고 Hello를 하면 왼쪽 정렬된 Hello를 볼 수 있다. 또한 %-10s뒤에 단어를 넣으면 일단 10개의 자리를 만들고나서 Hello를 넣고 공백을 채운후 World를 넣게 된다. 위 코드를 보면 World앞까지 10개의 자리가 있는 것을 확인할 수 있다.<br><br>

<Blockquote>소수점</Blockquote>
{% highlight python %}
>>> "%0.5f" %3.14159265358979323846264338327950288
'3.14159'
{% endhighlight %}
소수점을 전부 표시하고 싶지않고 어느 자리까지 표기하고 싶다면 .[원하는 자릿수]를 넣고 float를 뜻하는 f를 붙이면 원하는 자리까지 출력할 수 있다.<br><br>

<Blockquote>format</Blockquote>
위와같이 포매팅을 할 수 있지만 파이썬에는 format 함수가 있는데 이를 사용하면 편하게 포매팅을 할 수 있다.<br>
<br>

**숫자**
{% highlight python %}
>>> "I like number {0}" .format(7)
'I like number 7'
{% endhighlight %}
<br>

**문자열**
{% highlight python %}
>>> "I like number {0}" .format("one")
'I like number one'
{% endhighlight %}
<br>

**2개 이상의 값**
{% highlight python %}
>>> number = 7
>>> string = seven
>>> "I like number {0} ({1})" .format(number, string)
'I like number 7 (seven)'
{% endhighlight %}
2개 이상의 값을 넣을 경우는 {0}, {1}과 같이 순서대로 넣으면 값이 차례로 들어간다.<br><br>

**변수명**
{% highlight python %}
>>> "I like number {number} ({string})" .format(number = 7, string = "seven")
'I like number 7 (seven)'
{% endhighlight %}
변수를 정해서 값을 정해줄 수도있다<br><br>

**왼쪽 정렬**
{% highlight python %}
>>> "{0:<10}".format("Hello")
'Hello     '
{% endhighlight %}
format함수 또한 왼쪽정렬이 가능하다.<br><br>

**오른쪽 정렬**
{% highlight python %}
>>> "{0:>10}".format("Hello")
'     Hello'
{% endhighlight %}
왼쪽정렬에서는 <를 썼다면 오른쪽 정렬은 >를 사용하면 오른쪽 정렬된것을 확인할 수 있다.<br><br>

**공백 채우기**
{% highlight python %}
>>> "{0:~^10}".format("Hello")
'~~Hello~~~'
>>> "{0:!<10}".format("Hello")
'Hello!!!!!'
{% endhighlight %}
공백은 <, >, ^중 하나를 사용하기전에 원하는 문자를 넣고 정렬을 사용하면 공백을 채울 수 있다.<br><br>

**소수점 표현하기**
{% highlight python %}
>>> radi = 3.14159265358979323846264338327950288
>>> "{0:0.3f}".format(radi)
'3.142'
{% endhighlight %}
위에서 소수점을 표현한것처럼 f를 사용하면 원하는 자리까지 출력할 수 있다.<br><br>

{% highlight python %}
>>> radi = 3.14159265358979323846264338327950288
>>> "{0:10.3f}".format(radi)
'     3.142'
{% endhighlight %}
물론 위와같이 10자리를 만들어서 넣을 수도 있다.<br><br>

**{ }**
{% highlight python %}
>>> "{{  }}".format()
'{  }'
{% endhighlight %}
{}와 같은 중괄호 문자를 포매팅 문자가 아닌 문자 그대로 사용하고 싶으면 {{ }}이렇게 2개를 연속해서 사용하면된다.<br><br>

<Blockquote>f 문자열 포매팅</Blockquote>
{% highlight python %}
>>> number = 7
>>> string = "seven"
>>> f"I like {number} ({string})"
'I like 7 (seven)'
{% endhighlight %}
파이썬 3.6이상 버전부터는 f 문자열 포매팅을 사용할 수 있다. 그 아래 버전에서는 사용할 수 없다. 위와같이 문자열 앞에 f 접두사를 붙이면 문자열 포매팅 기능을 사용할 수 있다. f뒤에 오는 것은 큰따옴표도되고, 작은 따옴표도 가능하다.<br><br>

{% highlight python %}
>>> number = 7
>>> f'I like number {number + 1}'
'I like number 8'
{% endhighlight %}
위와같이 값을 더해서 출력도 가능하다.<br><br>

{% highlight python %}
>>> d = {'string' : 'one', 'number' : 1}
>>> f'I like {d["number"]} ({d["string"]})'
'I like 1 (one)'
{% endhighlight %}
딕셔너리는 f문자열 포매팅에서 위와같이 사용된다.<br><br>

{% highlight python %}
>>> f'{"Hello":<10}'
'Hello     '
>>> f'{"Hello":>10}'
'     Hello'
>>> f'{"Hello":^10}'
'  Hello   '
>>> 
{% endhighlight %}
정렬은 위와같이 사용된다.<br><br>

{% highlight python %}
>>> f'{"Hello":-^10}'
'--Hello---'
>>> f'{"Hello":~<10}'
'Hello~~~~~'
{% endhighlight %}
공백 또한 위와같이 사용된다.<br><br>

{% highlight python %}
>>> f'{radi:0.3f}'
'3.142'
>>> f'{radi:10.3f}'
'     3.142'
{% endhighlight %}
소수점과 공백을 넣은 소수점은 위와 같이 사용한다.<br><br>

{% highlight python %}
>>> f'{{  }}'
'{  }'
{% endhighlight %}
{ } 문자를 사용하고 싶으면 위와같이 두개를 동시에 사용하면된다.