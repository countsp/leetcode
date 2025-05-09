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



**pair**

```
priority_queue<pair<int, int>> pq;
pq.push({5, 0});
pq.push({1, 1});
pq.push({10, 2});

cout << pq.top().first;  // 输出 10（根据 pair.first 排序）
```

