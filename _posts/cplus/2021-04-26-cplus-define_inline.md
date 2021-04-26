---
layout: post
title: 매크로, 인라인[Define, Inline]
image: c++.png
date: 2021-04-26-22:34
tags: [c++, Define, Inline]
categories: cplus
---

<details>
<summary>English</summary>
<div markdown="1">
Define has the advantage of execution speed compared to general functions. How to use is as shown in the code below.
{% highlight c++ %}
#define SQUARE(x) ((x)*(x))

int main(){
    std::cout <<SQUARE(2) << std::end;
    return 0;
}
{% endhighlight %}
If you use the code above, the value 4 is displayed. Since the Define function is complex to define, the inline function emerged from the idea that it would be nice if it could be defined like a regular function. If the compiler judges that it is better to use inline, it is replaced and used, otherwise it is made to behave like a normal function.<br>
<br>
Inline also has the advantage of being fast in execution because it is used by replacing it with the desired code like a macro.<br>
<br>
Macro functions have the advantage of not having to think about the data type separately, but inline requires a separate data type, so data loss may occur in the data part. This is a problem solved by using templates. Also, the inline function must be written in the header file.
<br>


---------------------------------------------------------------------------------------------------
</div>
</details>
<br>
매크로는 일반적인 함수에 비해서 실행속도의 이점을 지니고 있다. 사용하는 방법은 아래의 코드와같이 사용하면된다.
{% highlight c++ %}
#define SQUARE(x) ((x)*(x))

int main(){
    std::cout <<SQUARE(2) << std::end;
    return 0;
}
{% endhighlight %}
위의 코드를 사용하면 값은 4가 출력될것이다. 매크로 함수는 정의하기가 복잡하니, 일반 함수처럼 정의가 된다면 좋겠다라는 생각에서 inline함수가 등장했다. 컴파일러가 판단하여 inline을 사용하는게 더 좋다는 판단이 내려지면 치환하여 사용해주고 그렇지 않다면 일반 함수처럼 동작하도록 만들어졌다.<br>
<br>
inline또한 매크로처럼 직접 원하는 코드로 실행하는 것이 아닌 치환하여 사용하기에 실행 속도에서 빠르다는 이점을 가지고있다.<br>
<br>
매크로 함수에는 따로 자료형에 대해 생각을 하지 않아도 된다는 이점을 지니고있는데 inline은 따로 자료형을 넣어줘야하기에 데이터부분에서 손실이 발생할 수 있다. 이는 템플릿을 사용하면 해결되는문제이다. 또한 inline함수는 헤더파일에서 작성해야한다.