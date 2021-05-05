---
layout: post
title: C++ 타입 캐스팅, 형변환[Type Casting]
image: c++.png
date: 2021-05-04-14:25
tags: [c++, Type]
categories: cplus
---

<details>
<summary>English</summary>
<div markdown="1">


---------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------
</div>
</details>

|Type|Explanation|Example|
|:---:|:---:|:---:|
|(signed) int <br>signed|부호가 있는 정수(양수, 음수)를 표현하며, 값의 범위는 컴파일러마다 다르다(대부분 4바이트).|```int i = -7;``` <br> ```signed int i = -6;``` <br> ```signed i = -5;```|
{:.mbtablestyle}


변수를 실행중에 바꿀 수 있는데 이를 casting(동적 형 변환, 타입 캐스팅(typecasting))이라고 한다.

{% highlight c++ %}
int int_num = 3;
dobule dou_num = 4.5;

int_num += dou_num;
{% endhighlight %}

예를 들어 위와같은 코드를 작성하면 VS컴파일러는 데이터 손실이 일어난다고 우리에게 경고해준다. 이는 프로그래머가 실수로 계산했을 땐 좋지만 의도한 일이라면 컴파일러에게 명시적으로 형변환을 한다고 알려줘야한다. 그 방법은 총 3가지가 있다.