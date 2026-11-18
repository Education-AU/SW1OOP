---
title: Reusing Person
template: default
---
This will indeed eliminate the duplication of person information, but as we can observe from the diagram the methods for retrieving the data `cpr`, `name`, `name`, `age` and so on still have to be implemented.

The reason for is that we artificially have to implement all the methods from `person` on `customer` and `employee` again to do nothing but to forward a method call to the `person` class.

To illustrate the forwarding, we show the example of the `get_name()` method

```cpp
class employee {
    public:
        std::string get_name() const { return person_.get_name(); } // just forwarding!
    private:
        person person_;
};
```
