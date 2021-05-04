---
layout: post
title: 리스트 인덱싱 & 슬라이싱[Python List Indexing & slicing]
image: python.jpg
date: 2021-05-03-21:57
tags: [python, Indexing, slicing]
categories: python
---


<details>
<summary>English</summary>
<div markdown="1">

List indexing & slicing
=====



-----------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------
</div>
</details>



리스트 인덱싱 & 슬라이싱
=====

>인덱싱



문자열에서 사용한 인덱싱과 슬라이싱처럼

{% highlight python %}
>>> number = [1, 2, 3, 4, 5]
{% endhighlight %}

위와같이 사용하고 ```number[0] = 1```임을 기억해야한다.<br>
파이썬 말고 다른 언어 중 C++을 해봤다면 ```number[0] = 6```이렇게 인덱스에 값을 넣는 등 연산이 가능하다. 또한 파이썬은 인덱스에 음수도 넣을 수 있어

{% highlight python %}
>>> number = [1, 2, 3, 4, 5]
>>> number[-1] = 7
>>> number
[1, 2, 3, 4, 7]
{% endhighlight %}

위와같이 사용할 수 도있다.<br>

{% highlight python %}
>>> something = [1, 2, 3, ['a', 'b', 'c']]
>>> something[3]
['a', 'b', 'c']
{% endhighlight %}

파이썬에서는 리스트안에 또 다른 리스트를 가질 수 있어서 위와같이 3번째 인덱스를 출력하면 ```something```안에있는 리스트가 출력된다. 만약 ```something```안에 있는 리스트중에 ```b```를 출력하고 싶다면 아래와 같이 이중 배열식으로해서 값을 출력하면된다.


{% highlight python %}
>>> something = [1, 2, 3, ['a', 'b', 'c']]
>>> something[3][1]
'b'
{% endhighlight %}


{% highlight python %}
>>> something = [1, 2, 3, ['a', 'b', 'c', ['one', 'two', 'three']]]
>>> something[3][3][1]
'two'


>>> something = [1, 2, 3, ['a', 'b', 'c', ['one', 'two', 'three', ['Hello']]]]
>>> something[3][3][3][0]
'Hello'
{% endhighlight %}

3중, 4중도 가능하다.


>슬라이싱


리스트 슬라이싱은 문자열 슬라이싱하고 거의 동일하다.

{% highlight python %}
>>> something = [0, 1, 2, 3, 4, 5]
>>> something[0:3]
[0, 1, 2]
{% endhighlight %}

```[0:3]```의 의미는 인덱스 0의 자리부터 2번째 인덱스까지 출력한다는 뜻이다. (3은 포함되지 않는다.)

{% highlight python %}
>>> something = [0, 1, 2, 3, 4, 5]
>>> something[:3]
[0, 1, 2]
>>> something[3:]
[3, 4, 5]
{% endhighlight %}

위와같이 ```[시작 자리 : 끝 자리]``` 시작자리를 비우고 끝 자리만 넣을 시 맨 처음부터 끝 자리 전까지 출력이되고 시작 자리만 넣고 끝 자리를 넣지 않을시 시작 자리부터 인덱스 맨 끝까지 값이 출력된다. 물론 처음부터 끝까지 출력하고 싶으면 시작 자리와 끝 자리에 아무것도 입력하지 않으면 된다.

{% highlight python %}
>>> something = [0, 1, 2, ['one', 'two', 'three'], 3, 4, 5]
>>> something[2:5]
[2, ['one', 'two', 'three'], 3]
>>> something[3][:2]
['one', 'two']
{% endhighlight %}

리스트 안에 있는 리스트도 위와같이 사용가능하다.