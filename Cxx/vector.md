# std::vector

vector是表示数组的序列容器（Sequence Container），其大小（容量）可以改变。

vector中的元素使用连续的线性存储位置（和array相同），可以使用指向其元素的常规指针来访问它们的元素，并且和数组一样高效（相较于其他动态序列容器list、deques）。

vector的内部使用一个动态分配的数组来存储元素。这个数组在插入新元素时可能需要重新分配空间来增大容量，这意味着分配一个新的数组并将所有的原有元素移动至其中。因此这个任务花费较高的时间成本。

因此，实际上vector会分配一些额外的存储空间以适应可能的增长，也就是说，容器的实际容量可能大于严格需要的存储容量。

（与array相比，vector消耗更多的内存，以换取管理存储和实现高效动态增长的能力）

## Initialization
    
创建一个空vector：

```cpp
    # include <vector>
    std::vector<type> var;
    // type: 数据类型
    // var: 变量名
```



```cpp
    # include <vector>
    std::vector<type> var(max_volume);
    // type: 数据类型
    // var: 变量名
    // max_volume: 容器最大大小
```

