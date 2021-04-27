---
layout: post
title: 네임스페이스[namespace]
image: c++.png
date: 2021-04-27-14:03
tags: [c++, namespace]
categories: cplus
---

<details>
<summary>English</summary>
<div markdown="1">
Name collisions, i.e. when identifiers with the same name are in the same scope, occur when the compiler cannot clearly know what to use. In this case, Compiral generates an error to resolve the ambiguity, and this can be resolved by using namespaces.<br>
<br>
If you do not use 'using namespace', you should use it as follows.
{% highlight c++ %}
#include <iostream>

void main() {
	std::cout << "Hello" << std::endl;
	std::cout << "World!" << std::endl;
}
{% endhighlight %}
Because variables or functions in the standard library are included in the std namespace, you must add std:: when using cout. Therefore, you can conveniently use the code by using'using namespace'.
{% highlight c++ %}
#include <iostream>

using namespace std;

void main() {
	cout << "Hello" << endl;
	cout << "World!" << endl;
}
{% endhighlight %}
And it can be used not only in std in the standard library, but also in your namespace.<br>
<br>
There are two ways to use'using namespace'.<br>
<Blockquote>When using only'using std::cout'</Blockquote>
{% highlight c++ %}
#include <iostream>

using std::cout;

void main() {
	cout << "Hello" << std::endl;
	cout << "World!" << std::endl;
}
{% endhighlight %}
In this case, only cout can be used by excluding std before it.<br>
<Blockquote>When using'using namespace std'</Blockquote>
{% highlight c++ %}
#include <iostream>

using namespace std;

void main() {
	cout << "Hello" << endl;
	cout << "World!" << endl;
}
{% endhighlight %}
In addition, namespcae can also be aliased.<br>
For example, AAA::BBB::CCC can be used by replacing this -> namespace ABC = AAA::BBB::CCC.
{% highlight c++ %}
#include <iostream>

using namespace std;


namespace AAA {
	namespace BBB {
		namespace CCC {
			string some = "Hello World!";
		}
	}
}

void main() {

	namespace ABC = AAA::BBB::CCC;

	cout << ABC::some;
}
{% endhighlight %}



---------------------------------------------------------------------------------------------------
</div>
</details>
<br>

 이름 충돌 즉, 이름이 같은 식별자가 같은 스코프에 있으면 컴파일러가 명확하게 무엇을 사용해야하는지 알 수 없을 때 일어난다. 이럴때 컴파일러는 모호함을 해결하기 위해서 오류를 발생시키는데 네임스페이스를 이용하면 이를 해결할 수 있다.<br>
<br>
'using namespace'를 사용하지 않으면 아래와 같이 사용해야 한다.
{% highlight c++ %}
#include <iostream>

void main() {
	std::cout << "Hello" << std::endl;
	std::cout << "World!" << std::endl;
}
{% endhighlight %}
왜냐하면 표준라이브러리에 있는 변수 또는 함수는 std namespace안에 포함되어있기 때문에, cout을 사용할 때는 std::를 붙여야한다. 그렇기에 'using namespca'를 사용하여 코드를 편리하게 사용할 수 있다.
{% highlight c++ %}
#include <iostream>

using namespace std;

void main() {
	cout << "Hello" << endl;
	cout << "World!" << endl;
}
{% endhighlight %}
그리고 표준라이브러리에 있는 std뿐만 아니라 내가 만든 namespace에서도 사용가능하다.<br>
<br>
'using namespace'를 쓰는 방법은 두가지가 있다.<br>
<Blockquote>'using std::cout'만 사용하는 경우</Blockquote>
{% highlight c++ %}
#include <iostream>

using std::cout;

void main() {
	cout << "Hello" << std::endl;
	cout << "World!" << std::endl;
}
{% endhighlight %}
이런 경우는 cout만 앞에 std를 제외해서 사용가능하다.<br>
<Blockquote>'using namespace std'를 사용하는 경우</Blockquote>
{% highlight c++ %}
#include <iostream>

using namespace std;

void main() {
	cout << "Hello" << endl;
	cout << "World!" << endl;
}
{% endhighlight %}
std 라이브러리안에 있는 모든것을 std::를 사용하지않아도 변수나 함수를 사용할 수 있다.<br>
<br>
또한 namespcae는 별칭도 설정할 수 있다.<br>
예를 들어 AAA::BBB::CCC이것을 -> namespace ABC = AAA::BBB::CCC로 바꿔서 사용가능하다.
{% highlight c++ %}
#include <iostream>

using namespace std;


namespace AAA {
	namespace BBB {
		namespace CCC {
			string some = "Hello World!";
		}
	}
}

void main() {

	namespace ABC = AAA::BBB::CCC;

	cout << ABC::some;
}
{% endhighlight %}