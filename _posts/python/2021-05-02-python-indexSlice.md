---
layout: post
title: 파이썬 인덱싱, 슬라이싱[Python Indexing, slicing]
image: python.jpg
date: 2021-05-02-01:22
tags: [python, Indexing, slicing]
categories: python
---

<details>
<summary>English</summary>
<div markdown="1">

String indexing and slicing
=====

<Blockquote>Indexing</Blockquote>

Indexing means putting the number of digits in the \[\] parentheses to print the character in its place or insert the value.<br>
To make it easier to understand, if you describe it as a string "Hello World", it has an index value as shown below.


| H | e | l | l | o |   | W | o | r | l | d |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
{:.mbtablestyle}


Python counts numbers from zero.
{% highlight python %}
>>> string = "Hello World"
>>> string[4]
'o'
{% endhighlight %}
In Python as well as in C and C++, since arrays start at 0, H has an index value of 0. Then, if you want to print 'o' in "Hello World", you can print 'o' by putting 4 in \[ \] brackets.<br>
<br>
Not in C or C++, but in Python, you can put in the value of an index. Then, 0 or -0 becomes 'H' unconditionally, so if you extract the value of -1, 'd' is output.

{% highlight python %}
>>> string = "Hello World
>>> string[-1]
'd'
{% endhighlight %}
Python prints even if you put a negative (-) value in the index. In the example below, if you put'-1' in parentheses, you can see that'd' is output, which is the first character counted from the back, so 'd' is output.


<Blockquote>Slicing</Blockquote>
Slicing means getting the value of a specific section of a string. Of course, indexing above doesn't look like much difference, but if you only want to get'Hello' from "Hello World", you can also get the value by indexing, but it's not convenient.
{% highlight python %}
>>> string = "Hello World
>>> word = string[0] + string[1] + string[2] + string[3] + string[4]
>>> word
'Hello'
{% endhighlight %}

In this way, 0, 1, 2, 3, 4 values can be added to the index, calculated, and then printed.<br>
However, slicing has the advantage of being able to bring it conveniently.
{% highlight python %}
>>> string = "Hello World"
>>> string[0:5]
'Hello'
{% endhighlight %}

You can easily get the value of the section you want by entering string\[starting digit: ending digit\]. Now, the values from 0 to 5 are taken here, starting from the starting digit, but the ending digit is not included, so the 'o' in the fourth digit is output.
{% highlight python %}
>>> string = "Hello World"
>>> string[3:8]
'lo Wo'
{% endhighlight %}

The number starting here does not have to be zero.
{% highlight python %}
>>> string = "Hello World"
>>> string[3:]
'lo World'
{% endhighlight %}

If you want to have a value from a specific start section to the end, you can have a value from the end of the string if you do not put anything in the ending digit and leave it blank as in the example above.
{% highlight python %}
>>> string = "Hello World">>> string[:8]
'Hello Wo'
{% endhighlight %}

Of course, on the contrary, if you want to have a value from the beginning, but you want to have a specific number of digits, you can leave the starting digit empty and put the value only in the ending digit, as in the example above.
{% highlight python %}
>>> string = "Hello World"
>>> string[:]
'Hello World'
{% endhighlight %}

If you want to have a string from start to finish, you should leave both blank and leave only ":"
{% highlight python %}
>>> string = "Hello World"
>>> string[3:-3]
'lo Wo'
{% endhighlight %}

As mentioned above, since Python can use negative values, it is also possible to have values as above.

-----------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------
</div>
</details>


문자열 인덱싱과 슬라이싱
=====

<Blockquote>인덱싱</Blockquote>

인덱싱은 \[ \]괄호에 자릿수를 넣어서 그 자리에 있는 문자를 출력이나 값을 넣는 것을 의미한다.<br>
일단 알기 쉽게 표로 설명하자면 "Hello World"라는 문자열로 설명하면 아래와 같이 인덱스 값을 가지게 된다.


| H | e | l | l | o |   | W | o | r | l | d |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
{:.mbtablestyle}

파이썬은 0부터 숫자를 센다.
{% highlight python %}
>>> string = "Hello World"
>>> string[4]
'o'
{% endhighlight %}
파이썬도 그렇고 C나 C++에서도 배열은 0부터 시작이기 때문에 H는 0의 인덱스 값을 가지게 된다. 그렇다면 "Hello World"에서 'o'를 출력하고 싶다면 \[ \]괄호안에 4를 넣어 'o'를 출력할 수 있다.<br>
<br>
c나 c++에서는 안되지만 파이썬에서는 인덱스의 값에 -를 넣을 수 있다. 그럼 0이나 -0은 무조건 'H'가 되니 -1의 값을 뽑는다면 'd'가 출력된다.


{% highlight python %}
>>> string = "Hello World
>>> string[-1]
'd'
{% endhighlight %}
파이썬은 인덱스에 마이너스(-)값을 넣어도 출력된다. 아래의 예제를 보면 괄호안에 '-1'를 넣으면 'd'가 출력되는 것을 볼 수 있는데 이는 뒤에서부터 세어 첫 번째인 문자를 가르키기 때문에 'd'가 출력된다.


<Blockquote>슬라이싱</Blockquote>
슬라이싱은 문자열에 있는 특정구간의 값을 가져오는것을 의미한다. 물론 위에 인덱싱하고 별반 다를게 없어 보이지만 "Hello World"에서 'Hello'만 가져오고싶다면 인덱싱으로도 값을 가져올 수 있지만 편리하지는 않다.
{% highlight python %}
>>> string = "Hello World
>>> word = string[0] + string[1] + string[2] + string[3] + string[4]
>>> word
'Hello'
{% endhighlight %}

이렇게 인덱스에 0, 1, 2, 3, 4값을 넣어서 연산한 후 출력을 할 수 있다.<br>
하지만 슬라이싱은 편리하게 가져올 수 있다는 장점이 있다.
{% highlight python %}
>>> string = "Hello World"
>>> string[0:5]
'Hello'
{% endhighlight %}

이렇게 string\[시작하는 자릿수:끝나는 자릿수\]를 입력해서 원하는 구간의 값을 쉽게 가져올 수 있다. 자 여기서 0~5까지의 값을 가져오게 되는데 시작하는 자릿수에서 시작하지만 끝나는 자릿수는 포함이 되지 않기때문에 4번째 자리에 있는 'o'까지만 출력하게 된다.
{% highlight python %}
>>> string = "Hello World"
>>> string[3:8]
'lo Wo'
{% endhighlight %}

여기서 시작하는 자리의 숫자가 꼭 0일 필요는 없다.
{% highlight python %}
>>> string = "Hello World"
>>> string[3:]
'lo World'
{% endhighlight %}

만약 특정 시작 구간에서 끝까지 값을 가지고 싶으면 끝나는 자릿수에 아무것도 넣지않고 위의 예제처럼 비워둔다면 문자열 끝까지 값을 가질 수 있다.
{% highlight python %}
>>> string = "Hello World">>> string[:8]
'Hello Wo'
{% endhighlight %}

물론 반대로 처음부터 값을 가지되, 특정 자릿수까지 가지고싶다면 위의 예제처럼 시작하는 자릿수를 비워두고 끝나는 자릿수에만 값을 넣으면 된다.
{% highlight python %}
>>> string = "Hello World"
>>> string[:]
'Hello World'
{% endhighlight %}

처음부터 끝까지 문자열을 가지고싶다면 둘다 비워두고 ":"만 남겨두면 된다.
{% highlight python %}
>>> string = "Hello World"
>>> string[3:-3]
'lo Wo'
{% endhighlight %}

위에 언급한 것처럼 파이썬은 마이너스값을 사용할 수 있기 때문에 위와같이 값을 가지는것도 가능하다.