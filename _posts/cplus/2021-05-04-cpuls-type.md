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

># Type

|Type|Explanation|Example|
|:---:|:---:|:---:|
|```(signed) int```<br><br>```signed```|Represents a signed integer (positive or negative), and the range of values varies from compiler to compiler (mostly 4 bytes).|```int i = -7;```<br><br>```signed int i = -6;``` <br><br>```signed i = -5;```|
|```(signed) short (int)```|Small range integer (mostly expressed as 2 bytes)|```short s = 10;```<br><br>```short int s = 11;```<br><br>```signed short s = 12;```<br><br>```signed short int s = 13;```|
|```(signed) long (int)```|Large range integers (mostly represented by 4 bytes)|```long l = -7L;```|
|```(signed) long long (int)```|Represents a very large range of integers. The specific range varies from compiler to compiler, but is at least larger than the ```long``` type (usually 8 bytes).|```long long ll = 14LL;```|
|```unsigned (int)```<br><br>```unsigned short (int)```<br><br>```unsigned long (int)```<br><br>```unsigned long long (int)```|Limit the range of integer types above to ```>=0```.|```unsigned int i = 2U;```<br><br>```unsigned j = 5U;```<br><br>```unsigned short s = 23U;```<br><br>```unsigned long l = 5400UL;```<br><br>```unsigned long long ll = 140ULL;```|
|```floaat```|single floating-point number|```float f = 7.2f;```|
|```double```|double Floating point number. Precision is at least greater than float.|```double d = 7.2;```|
|```long double```|long double Floating point number. Precision is at least greater than ```double```.|```long double d = 16.98L;```|
|```char```|Single character|```char ch = 'a';```|
|```char16_t```|16-bit single character|```char16_t c16 = u'a';```|
|```char32_t```|32-bit single character|```char32_t c32 = U'a';```|
|```wchar_t```|Single wide character. The specific size varies from compiler to compiler.|```wchar_t w = L'a';```|
|```bool```|Boolean type. It can be either true or false.|```bool b = true;```|
|```std::byte```|Represents one byte. Prior to C++17, a byte was represented as <br>```char``` or ```unsigned char```. <br>This expression gives the feeling of dealing with characters. On the other hand, when expressed as ```std::byte```, the meaning of <br>a byte of memory can be clearly revealed.|```std::byte b{42};```|
{:.mbtablestyle}


Variables can be changed during execution, which is called casting (dynamic type casting).

{% highlight c++ %}
int int_num = 3;
dobule dou_num = 4.5;

int_num += dou_num;
{% endhighlight %}

For example, if you write code like the above, the VS compiler warns us that data loss will occur. This is good if the programmer makes a mistake, but if it is intended, you need to tell the compiler to explicitly cast it. There are three ways to do that.


{% highlight c++ %}
float num = 3.14;

int a = (int)num;
{% endhighlight %}
It is the most commonly used method in C language, but it is also used in C++. This is not recommended.

{% highlight c++ %}
float num = 3.14;

int a = int(num);
{% endhighlight %}
It can be used as above, but it is rarely used.

{% highlight c++ %}
float num = 3.14;

int a = static_cast<int>(num);
{% endhighlight %}
The code above is long, but it is the clearest way to use this method.<br>
<br>


In addition to the above cases, there are times when the variable type is forcedly cast.<br>
For example, if the type ```short``` is assigned to ```long```, it is forcibly converted. This is because the precision of the ```long``` type is greater than that of the ```short```.

{% highlight c++ %}
short S_num;
long L_num = S_num; //No need for explicit casting.
{% endhighlight %}

---------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------
</div>
</details>


># Type

|Type|Explanation|Example|
|:---:|:---:|:---:|
|```(signed) int```<br><br>```signed```|부호가 있는 정수(양수, 음수)를 표현하며, 값의 범위는 컴파일러마다 다르다(대부분 4바이트).|```int i = -7;```<br><br>```signed int i = -6;``` <br><br>```signed i = -5;```|
|```(signed) short (int)```|작은 범위의 정수(대부분 2바이트로 표현)|```short s = 10;```<br><br>```short int s = 11;```<br><br>```signed short s = 12;```<br><br>```signed short int s = 13;```|
|```(signed) long (int)```|큰 범위의 정수(대부분 4바이트로 표현)|```long l = -7L;```|
|```(signed) long long (int)```|아주 큰 범위의 정수를 표현한다. 구체적인 범위는 컴파일러마다 다르나 <br>최소한 ```long```타입보다는 크다(주로 8바이트를 사용한다).|```long long ll = 14LL;```|
|```unsigned (int)```<br><br>```unsigned short (int)```<br><br>```unsigned long (int)```<br><br>```unsigned long long (int)```|위에 나온 정수 타입의 범위를 ```>=0```으로 제한한다.|```unsigned int i = 2U;```<br><br>```unsigned j = 5U;```<br><br>```unsigned short s = 23U;```<br><br>```unsigned long l = 5400UL;```<br><br>```unsigned long long ll = 140ULL;```|
|```floaat```|단정도(single), 부동소수점(floating-point number)|```float f = 7.2f;```|
|```double```|배정도(double), 부동소수점수. 정밀도가 최소한 float보다 크다.|```double d = 7.2;```|
|```long double```|롱배정도(long double) 부동소수점수. 정밀도가 최소한 double보다 크다.|```long double d = 16.98L;```|
|```char```|단일 문자|```char ch = 'a';```|
|```char16_t```|16비트 단일 문자|```char16_t c16 = u'a';```|
|```char32_t```|32비트 단일 문자|```char32_t c32 = U'a';```|
|```wchar_t```|단일 확장(single wide) 문자. 구체적인 크기는 컴파일러마다 다르다.|```wchar_t w = L'a';```|
|```bool```|부울 타입. true나 false 중 하나의 값을 가진다.|```bool b = true;```|
|```std::byte```|한 바이트를 표현한다. C++17 이전에는 한 바이트를 <br>```char```이나 ```unsigned char```로 표현했다. <br>이러한 표현은 문자를 다루는 듯한 느낌이 준다. 반면 ```std::byte```로 표현하면 <br>메모리의 한 바이트라는의미를 명확히 드러낼 수 있다.|```std::byte b{42};```|
{:.mbtablestyle}


변수를 실행중에 바꿀 수 있는데 이를 casting(동적 형 변환, 타입 캐스팅(typecasting))이라고 한다.

{% highlight c++ %}
int int_num = 3;
dobule dou_num = 4.5;

int_num += dou_num;
{% endhighlight %}

예를 들어 위와같은 코드를 작성하면 VS컴파일러는 데이터 손실이 일어난다고 우리에게 경고해준다. 이는 프로그래머가 실수로 계산했을 땐 좋지만 의도한 일이라면 컴파일러에게 명시적으로 형변환을 한다고 알려줘야한다. 그 방법은 총 3가지가 있다.


{% highlight c++ %}
float num = 3.14;

int a = (int)num;
{% endhighlight %}
C언어에서 제일 많이 사용하는 방법이지만, C++에서도 사용하는 방법이다. 별로 추천하지는 않는 방법이다.

{% highlight c++ %}
float num = 3.14;

int a = int(num);
{% endhighlight %}
위와같이도 사용할 수 있지만 거의 사용하지 않는 방법이다.

{% highlight c++ %}
float num = 3.14;

int a = static_cast<int>(num);
{% endhighlight %}
위의 코드는 길긴하지만 제일 명확하게 나타내는 방법이기에 이 방법을 사용하는게 좋다.<br>
<br>


위와같은 경우 말고 강제적으로 변수 타입을 캐스팅할 때도 있다.<br>
예를 들어 ```short```타입을 ```long```에 대입하면 강제적으로 변환된다. 이는 ```long```타입의 정밀도가 ```short```보다 크기때문이다.

{% highlight c++ %}
short S_num;
long L_num = S_num; //명시적 캐스팅이 필요없다.
{% endhighlight %}