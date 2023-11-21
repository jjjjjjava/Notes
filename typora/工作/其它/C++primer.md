![image-20231115103142806](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231115103142806.png)







当说到封装时，我们通常指的是将类的实现细节隐藏在类的接口之后，用户只能通过公共接口来访问类的功能，而无需关心其具体的实现细节。这种设计原则被称为信息隐藏或封装。

举个例子，考虑一个简单的图形库，其中有一个表示矩形的类 `Rectangle`。最初的设计如下：

```
cppCopy code// Rectangle.h
class Rectangle {
public:
    Rectangle(int width, int height);
    int calculateArea() const;

private:
    int width_;
    int height_;
};
cppCopy code// Rectangle.cpp
#include "Rectangle.h"

Rectangle::Rectangle(int width, int height) : width_(width), height_(height) {}

int Rectangle::calculateArea() const {
    return width_ * height_;
}
```

在这个设计中，用户级别的代码只需要包含 `Rectangle.h` 头文件，并使用 `Rectangle` 类的公共接口，例如：

```
cppCopy code#include "Rectangle.h"
#include <iostream>

int main() {
    Rectangle myRectangle(5, 10);
    std::cout << "Area: " << myRectangle.calculateArea() << std::endl;
    return 0;
}
```

现在，假设我们想要改变 `Rectangle` 类的实现细节，例如使用浮点数存储宽度和高度，而不是整数。我们可以轻松地在 `Rectangle.cpp` 中修改实现，而不影响用户级别的代码：

```
cppCopy code// Rectangle.cpp
#include "Rectangle.h"

Rectangle::Rectangle(float width, float height) : width_(width), height_(height) {}

float Rectangle::calculateArea() const {
    return width_ * height_;
}
```

用户级别的代码无需知道 `Rectangle` 类的实现细节发生了变化，因为它们仅依赖于类的公共接口。这种情况下，封装使得类的实现细节可以灵活地改变，而不会对使用类的代码造成影响。这是封装的一种优势，即改变实现而不影响用户级别的代码。