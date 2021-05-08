---
layout: post
title: 파이썬 리스트 연산[Python List Calculation]
image: python.jpg
date: 2021-05-08-21:05
tags: [python, listcalculation]
categories: python
---

<details>
<summary>English</summary>
<div markdown="1">

List Calculation
=====


In a list, you can also use symbols such as '+' or '*' to perform operations.

># +


{% highlight python %}
>>> num1 = [1, 2, 3]
>>> num2 = [4, 5, 6]
>>> num1 + num2
[1, 2, 3, 4, 5, 6]
{% endhighlight %}

You can perform an operation to add a list as above.

># *


{% highlight python %}
>>> num = [1, 2, 3]
>>> num * 3
[1, 2, 3, 1, 2, 3, 1, 2, 3]
{% endhighlight %}

Like strings, lists can be iterated multiple times through multiplication.
<br>
<br>

One thing to note here is that you can't calculate letters and numbers, so you have to put in a code such as converting numbers into letters.


-----------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------
</div>
</details>


리스트 연산
=====


리스트에서도 '+'나 '*'등 기호를 사용하여 연산을 할 수 있다.

># +


{% highlight python %}
>>> num1 = [1, 2, 3]
>>> num2 = [4, 5, 6]
>>> num1 + num2
[1, 2, 3, 4, 5, 6]
{% endhighlight %}

위와같이 리스트를 더하는 연산을 할 수 있다.

># *


{% highlight python %}
>>> num = [1, 2, 3]
>>> num * 3
[1, 2, 3, 1, 2, 3, 1, 2, 3]
{% endhighlight %}

문자열과 같이 리스트도 곱셈을 통해 여러번 반복할 수 있다.
<br>
<br>

여기서 주의해야할 점은 문자와 숫자를 연산할 수 없으니 숫자를 문자로 바꿔줘야하는 등의 코드를 넣어야한다.

