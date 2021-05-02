---
layout: post
title: ios_base::sync_with_stdio(false), cin.tie(NULL)
image: c++.png
date: 2021-05-02-15:57
tags: [c++, ios_base::sync_with_stdio(false), cin.tie(NULL)]
categories: cplus
---

<details>
<summary>English</summary>
<div markdown="1">

>## ios_base::sync_with_stdio(false)



Since standard streams are connected to each other, you can use ```C``` in ```C++```. However, when the above code is executed, the connection between streams is terminated, and C and C++ become independent buffers.

>### Buffer
###### The buffer is a place to temporarily store data when transferring data from A to B. For example, when viewing YouTube, the gray line represents the buffer.



However, you should not use C's ```scanf/prinf/puts/getchar/putchar, etc.``` because using C's I/O may result in unintended results. Also, the order of output may not come out properly in multi-threaded. Since the buffers used in C and C++ have C++ exclusive buffers, the number of buffers is reduced and the speed is increased.<br>
<br>

>## cin.tie(NULL)


Before executing the above code, ```cin``` and ```cout``` are connected. In other words, it unties one stream to be automatically flushed before ```I/O``` to another stream (which makes it visible to the console). Also, ```cin``` is the default value before executing the above code, so if you execute the following code,


{% highlight c++ %}
std::cout << "Hello";
std::cin >> something;
{% endhighlight %}


Since ```cout``` is flushed, ```''Hello''``` is displayed, and ```cin``` is entered, you can see the code behaves as intended. However, when executing the ```cin.tie(NULL)``` code, it does not flush after ```cout```, so ```cin``` is executed immediately, and ```''Hello''``` in the console.  will not be displayed.<br>
(But when I run it in VS, it outputs normally. Why is this... It shouldn't be.)
<br><br>

>### Tie
>>##### Flush before input request and output ```"Hello"```



>### Untie
>>##### Ask for ```cin``` input without ```cout``` flush. Basically, the output of ```cout``` is not output until the buffer is full or manually flushed. Therefore, if you want to flush before ```cin``` when untie, you have to do it manually.



First of all, the reason for using it has an advantage in terms of speed. C language ```scanf/printf``` is already fast by itself, so it doesn't matter, but in C++ ```cout``` doesn't make much difference, but ```cin``` is more than twice as slow. If you want to use it quickly in an algorithm problem, you can use ```cin.tie(NULL)```.<br>
However, if you just use this function, if you accidentally use the ```I/O``` function of the C language, unintended results will occur, so be careful about this point.<br>
<br>

In terms of speed, ```endl``` can also play a role in clearing the output buffer as well as outputting text, making it visible right on the screen, which is very slow. So, in terms of speed, it is better to use ```\n```.

---------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------
</div>
</details>

>## ios_base::sync_with_stdio(false)



표준 stream은 서로 이어져있기 때문에 ```C++```에서 ```C```를 사용가능한것이다. 하지만 위의 코드는 실행하면 stream간의 연결을 끝고 C와 C++은 독립적인 버퍼로 바뀐다.

>### 버퍼
###### 버퍼는 A에서 B로 데이터를 전송할 때 임시적으로 데이터를 보관하는 곳이다. 예를 들면 유튜브를 볼 때 회색선이 버퍼를 의미한다.



하지만 C의 ```scanf/prinf/puts/getchar/putchar 등``` C의 입출력을 사용하면 의도치않은 결과가 나올 수 있기때문에 사용하면 안된다. 또한 멀티 쓰레드에서는 출력 순서가 제대로 나오지 않을 수 있다. C와 C++을 사용하던 버퍼가 C++단독 버퍼를 가지기때문에 버퍼수는 줄어들고 속도는 빨라지는 이점을 가지고있다.<br>
<br>

>## cin.tie(NULL)


위코드를 실행하기전에는 ```cin```과 ```cout```이 연결되어있다. 즉, 한 스트림이 다른 스트림에 ```I/O```하기전에 자동으로 플러시(flush - 콘솔에 표시되도록하는 것)되게 하는걸 untie(풀게)한다. 또한 ```cin```은 ```cout```위코드를 실행하기전에는 디폴트값이기에 아래의 코드를 실행하면


{% highlight c++ %}
std::cout << "Hello";
std::cin >> something;
{% endhighlight %}


```cout```가 flush되어 ```"Hello"```가 출력되고 ```cin```이 들어가기에 원하는 의도대로 코드가 작동하는 것을 볼 수 있다. 하지만 ```cin.tie(NULL)```코드를 실행하면 ```cout```후에 flush를 해주지않기 때문에 바로 ```cin```이 실행 돼, 콘솔에는 ```"Hello"```가 출력되지 않게된다.<br>
(하지만 VS로 실행해 봤을 때는 정상적으로 출력된다. 왜이러지... 원래는 안되는게 맞다)
<br><br>

>### Tie
>>##### 입력 요구전에 flush해 ```"Hello"```출력



>### Untie
>>##### ```cout```flush가 안된채로 ```cin```입력을 요구한다. 기본적으로 ```cout```의 output은 버퍼가 가득차거나 수동으로 flush하기전까지는 출력이 안된다. 그러므로 untie일때 ```cin```전에 flush를 하고 싶으면 수동으로 flush해줘야한다.



일단 이걸 사용하는 이유는 속도면에서 이점을 가진다. C언어의 ```scanf/printf```는 이미 이 자체로 빠르기 때문에 상관없지만 C++에서 ```cout```은 별차이가 없지만 ```cin```은 2배이상 차이가 나기 때문에 알고리즘문제에서 빠르게 사용하고자 한다면 ```cin.tie(NULL)```을 사용하면된다.<br>
그렇다고 이 함수를 막쓰면 실수로 C언어의 ```I/O```기능을 사용한다면 의도치 않은 결과가 나오니 이 점은 주의해야한다.<br>
<br>

속도에서 ```endl```또한 개행문자 출력뿐만 아니라 출력 버퍼를 비우는 역할을 해서 화면에 바로 보이게 할 수있는데 이때문에 매우 느리다. 그래서 속도면에서만 본다면 ```\n```을 사용하는 것이 좋다.