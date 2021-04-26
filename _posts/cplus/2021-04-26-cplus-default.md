---
layout: post
title: 매개변수의 디폴트 값[Default Value]
image: c++.png
date: 2021-04-26-22:23
tags: [c++, Default_Value]
categories: cplus
---

<details>
<summary>English</summary>
<div markdown="1">


The default value of a parameter refers to calling the function with the specified default value in case the input of the parameter is omitted after calling the function.
{% highlight c++ %}
int Example(int num = 7){...}
{% endhighlight %}
If no argument is passed when calling the above function, 7 is assumed to be passed. The default value only needs to be written in the declaration part of the function.
{% highlight c++ %}
int Example(int num1, int num2, int num3 = 7){...}
int Example(int num1, int num2 = 7, int num3 = 7){...}
int Example(int num1 = 7, int num2 = 7, int num3 = 7){...}
{% endhighlight %}
As above, the default value can also be partially declared. But you can't do it like this:
{% highlight c++ %}
int Example(int num1 = 7, int num2, int num3){...}
int Example(int num1 = 7, int num2 = 7, int num3){...}
{% endhighlight %}
Because the arguments passed to the function are filled from left to right, the above cannot be applied.
<br>


---------------------------------------------------------------------------------------------------
</div>
</details>
<br>

매개변수의 디폴트 값이란 함수를 호출한 다음 매개변수의 입력을 생략할 경우, 지정된 디폴트 값을 넣어서 함수를 호출하는 것을 말한다.
{% highlight c++ %}
int Example(int num = 7){...}
{% endhighlight %}
위의 함수를 호출할 시 인자를 전달하지 않으면, 7이 전달 된 것으로 받아들인다. Default 값은 함수의 선언 부분에만 적으면 된다.
{% highlight c++ %}
int Example(int num1, int num2, int num3 = 7){...}
int Example(int num1, int num2 = 7, int num3 = 7){...}
int Example(int num1 = 7, int num2 = 7, int num3 = 7){...}
{% endhighlight %}
위와 같이 부분적으로도 Default값을 선언할 수 있다. 하지만 아래와 같이는 할 수 없다.
{% highlight c++ %}
int Example(int num1 = 7, int num2, int num3){...}
int Example(int num1 = 7, int num2 = 7, int num3){...}
{% endhighlight %}
왜냐하면 함수에 전달되는 인자는 왼쪽에서부터 오른쪽으로 채워지기 때문에 위와같이는 적용할 수 없다.