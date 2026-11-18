---
title: Visibility in Rectangle and Square
template: two-column
className: slide--two-column slide--rectangle-square-code
---

<style>
  .slide--rectangle-square-code .code-block {
    white-space: pre-wrap;
    overflow-wrap: anywhere;
    line-height: 1.25;
  }
</style>

```cpp
class rectangle {
// public section
public:
    rectangle(double height, double width, char color)
        : color(color), height_(height), width_(width) {}

    double area() {
        return height_ * width_;
    }
//protected section only visible locally and in children
protected:
    double circumference() {
        return 2 * (height_ + width_);
    }

    char color;

// private section NOT! visible in children
private:
    double height_;
    double width_;
};
```

<!-- column -->

```cpp
class square : public rectangle {
public:

    square(double size, char color) : rectangle(size, size, color) {}

    void print() {
        std::cout << "Area:" << area() << "Color:" << color << "Circumference:" << circumference();
        //                      public is ok ------protected is ok     --------   protected is ok

        //std::cout<<height<<width; does not compile height and width are private in rectangle
        //            private not ok
    }
};
```
