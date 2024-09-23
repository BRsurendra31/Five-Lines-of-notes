## unordered_map basics:
```cpp
#include <iostream>
#include <unordered_map>
using namespace std;

void Frequency(int arr[], int n) {
    unordered_map<int, int> map;
 
    // Count frequencies
    for (int i = 0; i < n; ++i) {
        map[arr[i]]++; //can write map[arr[i]] = map[arr[i]] + 1; or map[arr[i]] += 1;


    }
 
    // Print frequencies
    for (const auto& pair : map) {
        cout << pair.first << " " << pair.second << endl;
    }
}
```

**Example**
```cpp
unordered_map<int, int> map;
int arr[] = {1, 2, 2, 3, 1};
int n = 5;

for (int i = 0; i < n; ++i) {
    ++map[arr[i]];
}
```
Steps:

Initial State:

map is empty: {}
arr is {1, 2, 2, 3, 1}
First Iteration (i = 0):

arr[i] is 1
map[1] is accessed. Since 1 is not in the map, it is inserted with a default value of 0.
map[1] is incremented to 1.
map becomes {1: 1}
Second Iteration (i = 1):

arr[i] is 2
map[2] is accessed. Since 2 is not in the map, it is inserted with a default value of 0.
map[2] is incremented to 1.
map becomes {1: 1, 2: 1}
Third Iteration (i = 2):

arr[i] is 2
map[2] is accessed. 2 is already in the map with value 1.
map[2] is incremented to 2.
map becomes {1: 1, 2: 2}
Fourth Iteration (i = 3):

arr[i] is 3
map[3] is accessed. Since 3 is not in the map, it is inserted with a default value of 0.
map[3] is incremented to 1.
map becomes {1: 1, 2: 2, 3: 1}
Fifth Iteration (i = 4):

arr[i] is 1
map[1] is accessed. 1 is already in the map with value 1.
map[1] is incremented to 2.
map becomes {1: 2, 2: 2, 3: 1}

