```C++ runnable
#include <iostream>
class A
{
public:
    void foo() const { std::cout << "A"; }
 };

 class B
 { public:
    void foo() const { std::cout << "B"; }
 };

 class C : public A, public B
 {
    using A::foo;
 };

 int main()
 {
    C c;
    c.foo();
    return 0;
 }
```
