***
`unordered_set`是C++标准库中的一种容器，它提供了一种存储唯一元素的集合，并且以哈希表的方式来实现。在哈希表中，元素的存储位置是根据元素的键（key）通过哈希函数计算得到的哈希码决定的。

下面是`unordered_set`的一些重要特点和操作：

### 特点：
----
1. **唯一性**：`unordered_set`中的元素是唯一的，重复的元素只会被存储一次。
2. **快速查找**：哈希表提供了接近常数时间复杂度的查找操作（平均情况下），因此查找速度非常快。

### 主要操作：
----
1. **插入**：可以使用`insert()`函数向`unordered_set`中插入元素。
2. **删除**：使用`erase()`函数删除指定的元素。
3. **查找**：使用`find()`函数或迭代器进行元素的查找操作。
4. **大小**：使用`size()`函数获取`unordered_set`中元素的数量。
5. **遍历**：可以使用迭代器进行`unordered_set`中元素的遍历。

### 使用示例：
----
```cpp
#include <iostream>
#include <unordered_set>

int main() {
    std::unordered_set<int> mySet;

    // 插入元素
    mySet.insert(5);
    mySet.insert(10);
    mySet.insert(15);

    // 删除元素
    mySet.erase(10);

    // 查找元素
    auto it = mySet.find(5);
    if (it != mySet.end()) {
        std::cout << "Element found: " << *it << std::endl;
    }

    // 遍历集合
    for (auto& element : mySet) {
        std::cout << element << " ";
    }
    std::cout << std::endl;

    // 获取集合大小
    std::cout << "Size of set: " << mySet.size() << std::endl;

    return 0;
}
```

需要注意的是，`unordered_set`是无序的，即元素在内部存储时并不以任何特定顺序组织。如果需要有序性，可以考虑使用`std::set`，它是一个基于红黑树实现的有序集合容器。

`auto it = mySet.find(5)` 这行代码是在`unordered_set`中查找元素值为5的元素，并将结果保存在名为`it`的迭代器中。

- `mySet.find(5)`：这部分调用`unordered_set`的`find()`函数，寻找集合中值为5的元素。
- `auto it`：`auto` **关键字用于自动推断变量类型**，这里`it`是一个迭代器，它指向找到的元素位置。如果找到了值为5的元素，`it`指向该元素；如果没有找到，`it`将等于`mySet.end()`，表示未找到。

这个迭代器可以用于查看或操作找到的元素，或者用于检查元素是否存在于`unordered_set`中。通常，在使用迭代器之前，你需要检查`it`是否等于`mySet.end()`，以确保找到了有效的元素位置。

[[数组和set的区别]]
