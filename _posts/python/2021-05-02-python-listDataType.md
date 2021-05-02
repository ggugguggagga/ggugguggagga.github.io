---
layout: post
title: 리스트 자료형[List Data Type]
image: python.jpg
date: 2021-05-02-16:31
tags: [python, List_Data_Type]
categories: python
---

<details>
<summary>English</summary>
<div markdown="1">





-----------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------
</div>
</details>

리스트 자료형
=====


{% highlight python %}
>>> num = [1, 2, 3, 4, 5]
{% endhighlight %}
파이썬에서 리스트는 위와같이 변수에 대괄호안에 콤마로 이루어져있다. 생긴게 C++에서 배열과 비슷하게 생겼지만 크기를 지정해주지 않아도 된다.
그럼 자료형은 어떻게 하는가?

{% highlight python %}
>>> a = []
>>> b = [1, 2, 3]
>>> c = [1, 2, 3, 'one', 'two']
>>> d = ['one', 'two', 'three']
>>> e = [1, 2, ['one', 'two'] ]
{% endhighlight %}
위에 코드에 보이는 것 처럼 공백, 숫자, 혼합, 문자, 심지어 배열 자체도 넣을 수 있다.<br>
즉, 모든 유형이 가능하다.