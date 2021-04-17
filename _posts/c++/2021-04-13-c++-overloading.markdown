---
layout: post
title: 함수 오버로딩[Function Overloading]
image: c++.png
date: 2021-04-14-23:37
tags: [c++, overloading]
categories: cPlus
---

<details>
<summary>English</summary>
<div markdown="1">

Function Overloading is a C++ language feature that allows you to create functions with the same name but different parameters. In the C language, a function with the same name cannot be defined multiple times. In C++, even a function with the same name can be used in C+ becaause it is possible to distinguish what function is called through an argument passed when calling. For example, the following code can be used.

{% highlight c++ %}
int Example(int num){
    num++;
    return num;
}

int Exampe(int num1, int num2){
    return num1 + num2;
}
{% endhighlight %}
<br>
This way you can use function overloading in C++.

</div>
</details>
<br>

함수 오버로딩은 같은 이름을 가졌지만 다른 매개변수를 가진 함수를 만들 수 있는 C++언어의 기능이다. C언어에서는 같은 이름의 함수를 여러번 정의할 수 없다. C++에서는 동일한 이름을 가진 함수라도 호출시에 전달하는 인자를 통해서 무엇을 호출하는지 함수의 구분이 가능하기 때문에 C++에서는 사용할 수 있다. 예를 들자면 아래와 같은 코드를 예로 들 수 있다.

{% highlight c++ %}
int Example(int num){
    num++;
    return num;
}

int Exampe(int num1, int num2){
    return num1 + num2;
}
{% endhighlight %}
<br>
이런식으로 C++에서 함수 오버로딩을 사용할 수 있다.