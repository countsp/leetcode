239

**priority_queue**



**大根堆**

```
#include <queue>
#include <vector>
#include <iostream>
using namespace std;

int main() {
    priority_queue<int> pq;  // 默认是大根堆（最大堆）

    pq.push(5);
    pq.push(1);
    pq.push(10);

    while (!pq.empty()) {
        cout << pq.top() << " ";  // 每次输出最大值
        pq.pop();
    }

    return 0;
}
// 输出：10 5 1
```



**小根堆**

```
priority_queue<int, vector<int>, greater<int>> pq;
pq.push(5);
pq.push(1);
pq.push(10);

cout << pq.top();  // 输出 1（最小值）
```

### vector

**判断存在**
```
if (find(v.begin(), v.end(), 3) != v.end()) {
    // 元素 3 存在
}
```

**排序**
```
sort(intervals.begin(), intervals.end());
```
对于一个 vector<vector<int>> intervals，std::sort 默认会按 每个子 vector 的第一个元素（即 start）升序排列。

因为 std::vector<int> 本身支持按 字典序（lexicographical order）比较，这意味着：

会先比较 vec[0]；如果 vec[0] 相等，再比较 vec[1]；

**翻转** 189

std::reverse(begin, end)

### pair

```
priority_queue<pair<int, int>> pq;
pq.push({5, 0});
pq.push({1, 1});
pq.push({10, 2});

cout << pq.top().first;  // 输出 10（根据 pair.first 排序）
```


### unordered_map

count()判断元素存在？

```
unordered_map<char, int> freq;
    freq['A'] = 2;
    freq['B'] = 3;

    cout << freq.count('A') << endl; // 输出 1（存在）
    cout << freq.count('C') << endl; // 输出 0（不存在）
```

