---
title: Using Inherited Methods
template: two-column
---
All the public attributes and methods are available in customer and employee
with minimal effort

```cpp
int main() {
    employee employee(111111, "John Doe", 10000);
    std::cout << employee.get_cpr() << "\n";
    std::cout << employee.get_name() << "\n";
    std::cout << employee.get_age() << "\n";
    std::cout << employee.has_birthday() << "\n";
    customer customer(222222, "John Doe", 10000, 2000);
    std::cout << customer.get_cpr() << "\n";
    std::cout << customer.get_name() << "\n";
    std::cout << customer.get_age() << "\n";
    std::cout << customer.has_birthday() << "\n";
    return 0;
}
```

<!-- column -->

```text
111111
John Doe
10
0
222222
John Doe
10
0
```
