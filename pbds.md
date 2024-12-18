# 头文件

```cpp
#include <bits/extc++.h>
using namespace std;
using namespace __gnu_cxx;
using namespace __gnu_pbds;

// 优先队列
#include <ext/pb_ds/priority_queue.hpp> 

// 树
#include <ext/pb_ds/assoc_container.hpp> 
#include <ext/pb_ds/tree_policy.hpp> 
```

# 堆

```cpp
template <typename Value_Type,
    typename Cmp_Fn = std::less<Value_Type>,
    typename Tag = pairing_heap_tag ,
    typename Allocator = std::allocator<char> >
class priority_queue
```

### 解释

* Tag表示堆的类型
  * `binary_heap_tag`二叉堆
  * `binomial_heap_tag`二项堆
  * `rc_binomial_heap_tag`
  * `pairing heap tag`配对堆
  * `thin_heap_tag`
* Allocator不用管

### 用法

可以使用`begin()`和`end()`遍历

# 平衡树

```cpp
__gnu_pdds::tree<Key, T> 

template <
    typename Key, typename Mapped ,
    typename Cmp_Fn = std::less<Key>,
    typename Tag = rb_tree_tag ,
    template <
    typename Const_Node_Iterator ,
    typename Node_Iterator ,
    typename Cmp_Fn_ , typename Allocator_ >
    class Node_Update = null_tree_node_update ,
    typename Allocator = std::allocator <char> >
class tree;
```

### 解释

### 用法

- 与`std::map`用法基本相当，包括`begin()`,`end()`,`size()`,`empty()`,`clear()`,`find(const Key)`,`lower_bound(const Key)`, `upper_bound(const Key)`,`erase(iterator)`,`erase(const Key)`, `insert(const pair<Key, T>)`, `operator[](const Key)`
- `Tag`是`tree`的类型，有`rb_tree_tag`、`splay_tree_tag`、`ov_tree_tag`之一

### 改成set

把第二个模板参数改成`null_type`，此时迭代器的类型从`pair`变成`Key`。

