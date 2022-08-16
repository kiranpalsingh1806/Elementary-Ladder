
- [Array](#array)
  - [Find Kth Largest Element in Array](#find-kth-largest-element-in-array)
  - [Kadane Algorithm](#kadane-algorithm)
- [Bit Manipulation](#bit-manipulation)
  - [Check if ith bit is on](#check-if-ith-bit-is-on)
  - [Number of set bits in number](#number-of-set-bits-in-number)
  - [Unset the ith bit in number](#unset-the-ith-bit-in-number)
  - [Lexicographical next bit permutation](#lexicographical-next-bit-permutation)
  - [Round number to next highest power of 2](#round-number-to-next-highest-power-of-2)
  - [Bitwise OR of Vector using STL](#bitwise-or-of-vector-using-stl)
  - [Masks and Submasks Enumeration](#masks-and-submasks-enumeration)
- [Custom Comparator](#custom-comparator)
  - [Sorting by Comparator](#sorting-by-comparator)
  - [Sorting vector of strings based on number of ones - Comparator](#sorting-vector-of-strings-based-on-number-of-ones---comparator)
  - [Sorting Structure using Comparator](#sorting-structure-using-comparator)
  - [Sorting Vector Based on Another Vector](#sorting-vector-based-on-another-vector)
- [Data Structures](#data-structures)
  - [Prefix Sum 2D](#prefix-sum-2d)
  - [Fenwick Tree - Binary Indexed Tree](#fenwick-tree---binary-indexed-tree)
  - [Union Find - Disjoint Set Union](#union-find---disjoint-set-union)
  - [Policy Based Data Structure - Ordered Set](#policy-based-data-structure---ordered-set)
  - [Wavelet Matrix](#wavelet-matrix)
- [Grid and Matrix](#grid-and-matrix)
  - [Moving in four directions in grid](#moving-in-four-directions-in-grid)
  - [Knight Moves in Chessboard](#knight-moves-in-chessboard)
  - [Diagonals of Matrix (Top Left to Bottom Right)](#diagonals-of-matrix-top-left-to-bottom-right)
  - [Largest Square in Matrix With Only Ones](#largest-square-in-matrix-with-only-ones)
  - [Sudoku Box Pattern](#sudoku-box-pattern)
- [Sorting](#sorting)
  - [Merge Sort in Linked List](#merge-sort-in-linked-list)
- [Binary Search](#binary-search)
  - [Finding Pivot Element in Vector](#finding-pivot-element-in-vector)
  - [Binary Search - When middle goes out of range](#binary-search---when-middle-goes-out-of-range)
- [Linked List](#linked-list)
  - [Manipulation of head and tail in Linked List](#manipulation-of-head-and-tail-in-linked-list)
  - [Reverse Linked List](#reverse-linked-list)
- [Priority Queue](#priority-queue)
  - [Priority Queue with Comparator](#priority-queue-with-comparator)
  - [Priority Queue with Class Comparator](#priority-queue-with-class-comparator)
  - [Using Tuples in Priority Queue](#using-tuples-in-priority-queue)
- [Vector](#vector)
  - [Rotate Vector Left or right](#rotate-vector-left-or-right)
  - [Find element in vector and replace it](#find-element-in-vector-and-replace-it)
  - [Slicing of Vector in C++](#slicing-of-vector-in-c)
  - [Erase Duplicates in Vector](#erase-duplicates-in-vector)
  - [Common Elements in Vector](#common-elements-in-vector)
- [Dynamic Programming](#dynamic-programming)
  - [Longest Increasing Subsequence - LIS DP](#longest-increasing-subsequence---lis-dp)
  - [Partial Sum](#partial-sum)
- [Graphs](#graphs)
  - [Can We Go From Source To Destination](#can-we-go-from-source-to-destination)
  - [Print Euler Tour](#print-euler-tour)
  - [Breadth First Search](#breadth-first-search)
  - [DFS - First and Last Order](#dfs---first-and-last-order)
  - [Dijkstra's Algorithm](#dijkstras-algorithm)
  - [Lowest Common Ancestor](#lowest-common-ancestor)
  - [Number of Connected Components](#number-of-connected-components)
  - [Kruskal Algorithm - Minimum Spanning Tree](#kruskal-algorithm---minimum-spanning-tree)
  - [Euler path - Heirholzer Algorithm](#euler-path---heirholzer-algorithm)
  - [Bipartite Graph](#bipartite-graph)
  - [Bellman Ford Algorithm](#bellman-ford-algorithm)
- [Recursion](#recursion)
  - [Maximum Digit in Number](#maximum-digit-in-number)
- [Binary Trees](#binary-trees)
  - [Find Path From Root To Target Node](#find-path-from-root-to-target-node)
- [String](#string)
  - [stringstream Implementation](#stringstream-implementation)
  - [Convert Vector to Unordered Set](#convert-vector-to-unordered-set)
  - [Euler Phi Function](#euler-phi-function)
  - [Finding if element inserted in set or not](#finding-if-element-inserted-in-set-or-not)
- [String Algorithm](#string-algorithm)
  - [Rabin Karp Algorithm](#rabin-karp-algorithm)
  - [Z Function - Prefix Function](#z-function---prefix-function)
  - [Adding numbers in string](#adding-numbers-in-string)
  - [Longest Prefix Suffix](#longest-prefix-suffix)
- [Lambda Function](#lambda-function)
  - [Definition of Lambda Function](#definition-of-lambda-function)
  - [Lambda Function to Check if Vector is Permutation](#lambda-function-to-check-if-vector-is-permutation)
- [Heaps](#heaps)
  - [Max Heap and Min Heap](#max-heap-and-min-heap)
  - [Convert Vector to Heaps in C++](#convert-vector-to-heaps-in-c)
- [Permutation](#permutation)
  - [Next Permutation](#next-permutation)
- [Mathematics](#mathematics)
  - [Chicken McNugget Theorem](#chicken-mcnugget-theorem)
  - [Sum of Two Numbers with Given Base](#sum-of-two-numbers-with-given-base)
- [Prime Numbers](#prime-numbers)
  - [Prime Numbers in Range](#prime-numbers-in-range)
- [Base Conversion](#base-conversion)
  - [Convert To Decimal From Base K](#convert-to-decimal-from-base-k)
- [GCD and LCM](#gcd-and-lcm)
  - [Maximum GCD in range [L, R]](#maximum-gcd-in-range-l-r)
  - [Dirichlet's Convolution](#dirichlets-convolution)
  - [Euler Totient Function](#euler-totient-function)
- [Geometry](#geometry)
  - [Point Structure in Geometry](#point-structure-in-geometry)
- [Mathematical Equations](#mathematical-equations)
  - [Find x and y in a.x + b.y = N](#find-x-and-y-in-ax--by--n)
- [Miscellaneous](#miscellaneous)
  - [Numeric Limits](#numeric-limits)
  - [Median of an array](#median-of-an-array)
  - [Reverse a number](#reverse-a-number)
  - [Generating Random Numbers in Range](#generating-random-numbers-in-range)

## Array

### Find Kth Largest Element in Array

```cpp
int findKthLargest(vector<int>& A, int k) {
    nth_element(begin(A), begin(A) + k - 1, end(A), greater<int>());
    return A[k - 1];
}
```

### Kadane Algorithm
```cpp
int maxSumSubarray (vector<int> A) {
	int n = A.size();
	int local_max = 0;
	int global_max = -1e9;
    for(int i = 0; i < n; i++) {
        local_max = max(A[i], A[i] + local_max);

        if(local_max > global_max) {
            global_max = local_max;
        }
    }
    return global_max;
}


void solve()
{ 
	int n;
	cin >> n;
	vector<ll> a(n);
	for(int i = 0; i < n; i++) {
		cin >> a[i];
	}

	ll mx = maxSumSubArray(a);
	cout << mx << "\n";
}
```

## Bit Manipulation

### Check if ith bit is on
```cpp
for(int i = 0; i < 32; i++) {
    if(x & (1 << i)) {
        // True if ith bit of x is set
    }
}
```

### Number of set bits in number
```cpp
int setbitsCnt = __builtin_popcount(x);
long int setbitsCnt = __builtin_popcountl(x);
long long setbitsCnt = __builtin_popcountll(x);
```

### Unset the ith bit in number

```cpp
int num = 104;
// Unset the 6th bit (bits start from 0 index)
int pos = 6;
cout << "Before : " << bitset<8>(num) << "\n";
num &= (~(1 << pos));
cout << "After :: " << bitset<8>(num) << "\n";
```

### Lexicographical next bit permutation

```cpp
// Current permutation of bits
  unsigned int v = 11;
  
  // Next permutation of bits
  unsigned int w;
  
  unsigned int t = (v | (v - 1)) + 1;  
  w = t | ((((t & -t) / (v & -v)) >> 1) - 1);
  
  
  cout << "v : " << bitset<8>(v) << "\n";
  cout << "w : " << bitset<8>(w) << "\n";
```

### Round number to next highest power of 2
```cpp

unsigned int v = 43;
v--;
v |= v >> 1;
v |= v >> 2;
v |= v >> 4;
v |= v >> 8;
v |= v >> 16;
v++;

cout << v << "\n";
// Output - 64 (which is power of 2).
```

### Bitwise OR of Vector using STL
```cpp
int result = reduce(nums.begin(), nums.end(), 0, bit_or());
```

### Masks and Submasks Enumeration

```cpp
void bitmasks() {
	int n = 5;
	vector<vector<int>> masks(1 << n, vector<int>()); // 32 ( 2 ^ 5)

	// Traverse all masks
	for(int mask = 0; mask < (1 << n); mask++) {
		for(int i = 0; i < n; i++) {
			if(mask & (1 << i)) {
				masks[mask].push_back(i);
				cout << mask << " mask has this bit on => " << i << "\n";
			}
		}
	}

	vector<vector<int>> submasks(1 << n, vector<int>()); 

	// Traverse all submasks of masks
	for(int mask = 1; mask < (1 << n); mask++) {
		for(int submask = mask; submask; submask = (submask - 1) & mask) {
			submasks[mask].push_back(submask);
			cout << mask << " mask has this submask => " << submask << "\n";
		}
	}
}
```

## Custom Comparator

### Sorting by Comparator 
```cpp
bool cmp(const pair<string, long> &p1, const pair<string, long> &p2)
{
    if(p1.second!=p2.second)
        return p1.second < p2.second;
    return p1.first < p2.first;
}

sort(vect.begin(), vect.end(), cmp);
```

### Sorting vector of strings based on number of ones - Comparator
```cpp
void solve()
{
	int n;
	cin >> n;
	vector<string> s(n);

	for(int i = 0; i < n; i++) {
		cin >> s[i];
	}
	sort(s.begin(), s.end(), [&](string x, string y) {
        return count(x.begin(), x.end(), '1') < count(y.begin(), y.end(), '1');
    });

    for(int i = 0; i < n; i++) {
    	cout << s[i] << "\n";
    }
}

// Input
// 5
// 10101
// 10000000
// 010101
// 00111111
// 11000000000

// Output
// 10000000
// 11000000000
// 10101
// 010101
// 00111111
```

### Sorting Structure using Comparator
```cpp
struct city {
	string name;
	int score, index;
};

int n;

bool comp(const city a, const city b) {
	if(a.name != b.name) {
		return a.name < b.name;
	}
	return a.score > b.score;
}

void solve() {
	cin >> n;
	vector<city> cities(n);
	for(int i = 0; i < n; i++) {
		cin >> cities[i].name >> cities[i].score;
		cities[i].index = i + 1;
	}	

	sort(cities.begin(), cities.end(), comp);

	for(int i = 0; i < n; i++) {
		cout << cities[i].index << "\n";
	}
}

// Input
// 6
// khabarovsk 20
// moscow 10
// kazan 50
// kazan 35
// moscow 60
// khabarovsk 40

// Output
// 3
// 4
// 6
// 1
// 5
// 2

```

### Sorting Vector Based on Another Vector
```cpp
int main() {
    int n = 7;
    vector<int> a = {4, 8, 1, 3, 2, 9, 11};
    
    vector<int> ind(n);
    iota(ind.begin(), ind.end(), 0);
    for(auto a: ind) {
        cout << a << " ";
    }
    cout << "\n";
    
    sort(ind.begin(), ind.end(), [&](int i, int j) {
        return a[i] > a[j];
    });

    for(auto a: ind) {
        cout << a << " ";
    }
    cout << "\n";
}
```

## Data Structures

### Prefix Sum 2D
```cpp
#include<bits/stdc++.h>
using namespace std;

constexpr int MAX_SIDE = 1000;
int prefixSum2D[MAX_SIDE + 1][MAX_SIDE + 1];
int array2D[MAX_SIDE + 1][MAX_SIDE + 1];

void solve()
{
	int N;
	int Q;
	cin >> N >> Q;
	// read the 2D array
	for (int i = 1; i <= N; i++) {
		for (int j = 1; j <= N; j++) {
			cin >> array2D[i][j];
		}
	}

	// build the prefix sum array
	for (int i = 1; i <= N; i++) {
		for (int j = 1; j <= N; j++) {
			prefixSum2D[i][j] = array2D[i][j]
						+ prefixSum2D[i - 1][j]
						+ prefixSum2D[i][j - 1]
						- prefixSum2D[i - 1][j - 1];
		}
	}

	for (int q = 0; q < Q; q++) {
		int x1, x2, y1, y2;
		cin >> x1 >> y1 >> x2 >> y2;
		cout << prefixSum2D[x2][y2]
				- prefixSum2D[x1-1][y2]
				- prefixSum2D[x2][y1-1]
				+ prefixSum2D[x1-1][y1-1] << '\n';
	}

}

int main(void) {
	solve();
}
```

### Fenwick Tree - Binary Indexed Tree

```cpp
struct FenwickTree {
	vector<int> bit;  // binary indexed tree
	int n;

	FenwickTree(int n) {
		this->n = n + 1;
		bit.assign(n + 1, 0ll);
	}

	void add(int idx, int val) {
		for (++idx; idx < n; idx += idx & -idx)
			bit[idx] += val;
	}

	void range_add(int l, int r, int val) {
		add(l, val);
		add(r + 1, -val);
	}

	int get(int idx) { //
		int ret = 0;
		for (++idx; idx > 0ll; idx -= idx & -idx)
			ret += bit[idx];
		return ret;
	}
};
```

Problems
[Chef and Queries](https://www.codechef.com/START5B/problems/CHEFQUER)

### Union Find - Disjoint Set Union
```cpp
// Using Structure
struct UnionFind{
    int num;
    vector<int> rs, parent;
    UnionFind(int n): num(n), rs(n, 1), parent(n, 0) {
        iota(parent.begin(), parent.end(), 0);
    }

    int find(int x) {
        return (x == parent[x] ? x : parent[x] = find(parent[x]));
    }

    bool same(int x, int y) {
        return find(x) == find(y);
    }

    void unite(int x, int y) {
        x = find(x); y = find(y);
        if (x == y) return;
        if (rs[x] < rs[y]) swap(x, y);
        rs[x] += rs[y];
        parent[y] = x;
        num--;
    }

    int size(int x) {
        return rs[find(x)];
    }

    int countSets() const {
        return num;
    }
};

// Using class
class UnionFind {
    private:
        vector<int> id, rank;
        int cnt;
    public:
        UnionFind(int cnt) : cnt(cnt) {
            id = vector<int>(cnt);
            rank = vector<int>(cnt, 0);
            for (int i = 0; i < cnt; ++i) id[i] = i;
        }
        int find(int p) {
            if (id[p] == p) return p;
            return id[p] = find(id[p]);
        }
        int getCount() { 
            return cnt; 
        }
        bool connected(int p, int q) { 
            return find(p) == find(q); 
        }
        void connect(int p, int q) {
            int i = find(p), j = find(q);
            if (i == j) return;
            if (rank[i] < rank[j]) {
                id[i] = j;  
            } else {
                id[j] = i;
                if (rank[i] == rank[j]) rank[j]++;
            }
            --cnt;
        }
};

// Union Find that also return the vector of size of components.
class UnionFind {
    vector<int> id, size;
public:
    UnionFind(int n) : id(n), size(n, 1) {
        for (int i = 0; i < n; ++i) id[i] = i;
    }
    void connect(int a, int b) {
        int x = find(a), y = find(b);
        if (x == y) return;
        id[x] = y;
        size[y] += size[x];
    }
    int find(int a) {
        return id[a] == a ? a : (id[a] = find(id[a]));
    }
    vector<int> &getSizes() {
        return size;
    }
};
```

### Policy Based Data Structure - Ordered Set

```cpp
#include <ext/pb_ds/assoc_container.hpp> // Common file
#include <ext/pb_ds/tree_policy.hpp>
#include <functional> // for less

using namespace __gnu_pbds;
using namespace std;

typedef tree<int, null_type, less<int>, rb_tree_tag, tree_order_statistics_node_update> ordered_set;

int main()
{
    ordered_set p;
    p.insert(5);
    p.insert(2);
    p.insert(6);
    p.insert(4);
 
    // value at 3rd index in sorted array.
    cout << "The value at 3rd index ::" << *p.find_by_order(3) << endl;
 
    // index of number 6
    cout << "The index of number 6::" << p.order_of_key(6) << endl;
 
    // number 7 not in the set but it will show the index number if it was there in sorted array.
    cout << "The index of number seven ::" << p.order_of_key(7) << endl;
 
    return 0;
}
```

Problems
1. [Maximum Possible Sweetness](https://www.codechef.com/START7B/problems/MAXSWT)
2. [Number of Pairs](https://codeforces.com/contest/1538/problem/C)
3. [Nested Segments](https://codeforces.com/contest/652/problem/D)
4. [Optimal Subsequences](https://codeforces.com/contest/1262/problem/D2)

### Wavelet Matrix

```cpp
#include <bits/stdc++.h>
using namespace std;


struct SuccinctIndexableDictionary {
  size_t length;
  size_t blocks;
  vector< unsigned > bit, sum;
 
  SuccinctIndexableDictionary() = default;
 
  SuccinctIndexableDictionary(size_t length) : length(length), blocks((length + 31) >> 5) {
    bit.assign(blocks, 0U);
    sum.assign(blocks, 0U);
  }
 
  void set(int k) {
    bit[k >> 5] |= 1U << (k & 31);
  }
 
  void build() {
    sum[0] = 0U;
    for(int i = 1; i < blocks; i++) {
      sum[i] = sum[i - 1] + __builtin_popcount(bit[i - 1]);
    }
  }
 
  bool operator[](int k) {
    return (bool((bit[k >> 5] >> (k & 31)) & 1));
  }
 
  int rank(int k) {
    return (sum[k >> 5] + __builtin_popcount(bit[k >> 5] & ((1U << (k & 31)) - 1)));
  }
 
  int rank(bool val, int k) {
    return (val ? rank(k) : k - rank(k));
  }
};

template< typename T, int MAXLOG >
struct WaveletMatrix {
  size_t length;
  SuccinctIndexableDictionary matrix[MAXLOG];
  int mid[MAXLOG];
 
  WaveletMatrix() = default;
 
  WaveletMatrix(vector< T > v) : length(v.size()) {
    vector< T > l(length), r(length);
    for(int level = MAXLOG - 1; level >= 0; level--) {
      matrix[level] = SuccinctIndexableDictionary(length + 1);
      int left = 0, right = 0;
      for(int i = 0; i < length; i++) {
        if(((v[i] >> level) & 1)) {
          matrix[level].set(i);
          r[right++] = v[i];
        } else {
          l[left++] = v[i];
        }
      }
      mid[level] = left;
      matrix[level].build();
      v.swap(l);
      for(int i = 0; i < right; i++) {
        v[left + i] = r[i];
      }
    }
  }
 
  pair< int, int > succ(bool f, int l, int r, int level) {
    return {matrix[level].rank(f, l) + mid[level] * f, matrix[level].rank(f, r) + mid[level] * f};
  }
 
  // v[k]
  T access(int k) {
    T ret = 0;
    for(int level = MAXLOG - 1; level >= 0; level--) {
      bool f = matrix[level][k];
      if(f) ret |= T(1) << level;
      k = matrix[level].rank(f, k) + mid[level] * f;
    }
    return ret;
  }
 
  T operator[](const int &k) {
    return access(k);
  }
 
  // count i s.t. (0 <= i < r) && v[i] == x
  int rank(const T &x, int r) {
    int l = 0;
    for(int level = MAXLOG - 1; level >= 0; level--) {
      tie(l, r) = succ((x >> level) & 1, l, r, level);
    }
    return r - l;
  }
 
  // k-th(0-indexed) smallest number in v[l,r)
  T kth_smallest(int l, int r, int k) {
    assert(0 <= k && k < r - l);
    T ret = 0;
    for(int level = MAXLOG - 1; level >= 0; level--) {
      int cnt = matrix[level].rank(false, r) - matrix[level].rank(false, l);
      bool f = cnt <= k;
      if(f) {
        ret |= T(1) << level;
        k -= cnt;
      }
      tie(l, r) = succ(f, l, r, level);
    }
    return ret;
  }
 
  // k-th(0-indexed) largest number in v[l,r)
  T kth_largest(int l, int r, int k) {
    return kth_smallest(l, r, r - l - k - 1);
  }
 
  // count i s.t. (l <= i < r) && (v[i] < upper)
  int range_freq(int l, int r, T upper) {
    int ret = 0;
    for(int level = MAXLOG - 1; level >= 0; level--) {
      bool f = ((upper >> level) & 1);
      if(f) ret += matrix[level].rank(false, r) - matrix[level].rank(false, l);
      tie(l, r) = succ(f, l, r, level);
    }
    return ret;
  }
 
  // count i s.t. (l <= i < r) && (lower <= v[i] < upper)
  int range_freq(int l, int r, T lower, T upper) {
    return range_freq(l, r, upper) - range_freq(l, r, lower);
  }
 
  // max v[i] s.t. (l <= i < r) && (v[i] < upper)
  T prev_value(int l, int r, T upper) {
    int cnt = range_freq(l, r, upper);
    return cnt == 0 ? T(-1) : kth_smallest(l, r, cnt - 1);
  }
 
  // min v[i] s.t. (l <= i < r) && (lower <= v[i])
  T next_value(int l, int r, T lower) {
    int cnt = range_freq(l, r, lower);
    return cnt == r - l ? T(-1) : kth_smallest(l, r, cnt);
  }
};
 

int main() 
{
    const int n = 7;
    
    vector<int> A(n);
    
    for(auto &a : A) cin >> a;
    
    WaveletMatrix<int, n> mat(A);
    
    auto ans = mat.kth_smallest(0, 4, 3);
    cout << "Kth smallest element in range [L, R) : " << ans << "\n";
    
    auto rangefreq = mat.range_freq(0, n, 5);
    cout << "Frequency of element in range [L, R) : " << rangefreq << "\n";
    
    auto kthmax = mat.kth_largest(0, n, 2);
    cout << "Kth Largest Element in Vector : " << kthmax << "\n";
    
}
```

## Grid and Matrix 

### Moving in four directions in grid

```cpp
int dirs[4][2] = {{0,1},{0,-1},{1,0},{-1,0}};

for (auto &dir : dirs) {
    int a = x + dir[0], b = y + dir[1];
    // Here x and y is our current location.
}

int dirs[8][2] = { {-1, -1}, {-1, 0}, {-1, 1}, {0, -1}, {0, 1}, {1, -1}, {1, 0}, {1, 1}};

for (auto &dir : dirs) {
     int a = x + dir[0];
     int b = y + dir[1];
}
```

### Knight Moves in Chessboard

```cpp
int dirs[8][2] = {{-2,1}, {-1,2}, {1,2}, {2,1}, {2,-1}, {1,-2}, {-1,-2}, {-2,-1}};

for (auto &dir : dirs) {
    int a = x + dir[0], b = y + dir[1];
    // Here x and y is our current location.
}
```

### Diagonals of Matrix (Top Left to Bottom Right)
```cpp
int M = 5, N = 3;
cout << "Lower Triangle Diagonals" << "\n";
for (int i = 0; i < M; ++i) {
    cout << "------\n";
    for (int x = i, y = 0; x < M && y < N; ++x, ++y) {
    cout << x << " " << y << "\n";
    }
}

cout << "-------\n";
cout << "Upper Triangle Diagonals" << "\n";
for (int j = 1; j < N; ++j) {
    vector<int> v;
    cout << "------\n";
    for(int x = 0, y = j; x < M && y < N; ++x, ++y) {
    cout << x << " " << y << "\n";
    }
}
```

### Largest Square in Matrix With Only Ones

```cpp
int maximalSquare(vector<vector<char>>& matrix) {
    int M = matrix.size();
    int N = matrix[0].size();
    
    int ans = 0;
    
    vector<vector<int>> mat(M, vector<int>(N));
    
    for(int i = 0; i < M; i++) {
        for(int j = 0; j < N; j++) {
            mat[i][j] = matrix[i][j] - '0';
        }
    }
    
    for(int i = 0; i < M; i++) {
        for(int j = 0; j < N; j++) {
            if(i > 0 && j > 0 && mat[i][j] != 0) {
                mat[i][j] = min({mat[i][j - 1], mat[i - 1][j], mat[i - 1][j - 1]}) + 1;
            }
            
            ans = max(ans, mat[i][j]);
        }
    }
    
    // For side of largest square
    // return ans

    // For area of largest square
    return ans * ans; 
}
```

### Sudoku Box Pattern
```cpp
int box[9][9] = {};
for(int i = 0; i < 9; i++) {
    for(int j = 0; j < 9; j++) {
    box[i][j] = (i / 3 ) * 3+ (j / 3);
    }
}

for(int i = 0; i < 9; i++) {
    for(int j = 0;j < 9; j++) {
    cout << box[i][j] << " ";
    }
    cout << "\n";
}

// Output
// 0 0 0 1 1 1 2 2 2 
// 0 0 0 1 1 1 2 2 2 
// 0 0 0 1 1 1 2 2 2 
// 3 3 3 4 4 4 5 5 5 
// 3 3 3 4 4 4 5 5 5 
// 3 3 3 4 4 4 5 5 5 
// 6 6 6 7 7 7 8 8 8 
// 6 6 6 7 7 7 8 8 8 
// 6 6 6 7 7 7 8 8 8
```

## Sorting

### Merge Sort in Linked List
```cpp
class Solution {
    ListNode* splitList(ListNode *head) {
        ListNode dummy, *p = &dummy, *q = &dummy;
        dummy.next = head;
        while (q && q->next) {
            q = q->next->next;
            p = p->next;
        }
        auto next = p->next;
        p->next = NULL;
        return next;
    }
    ListNode *mergeList(ListNode *a, ListNode *b) {
        ListNode head, *tail = &head;
        while (a && b) {
            ListNode *node;
            if (a->val <= b->val) {
                node = a;
                a = a->next;
            } else {
                node = b;
                b = b->next;
            }
            tail->next = node;
            tail = node;
        }
        if (a) tail->next = a;
        if (b) tail->next = b;
        return head.next;
    }
public:
    ListNode* sortList(ListNode* head) {
        if (!head || !head->next) return head;
        auto b = splitList(head);
        return mergeList(sortList(head), sortList(b));
    }
};
```

## Binary Search

### Finding Pivot Element in Vector

```cpp
int L = 0, R = nums.size() - 1, pivot;
while (L < R) {
    int M = L + (R - L) / 2;
    if (nums[M] < nums[R]) R = M;
    else L = M + 1;
}
pivot = L;
```

### Binary Search - When middle goes out of range

```cpp
int M = (L + R) / 2;
// signed integer overflow: 1063376696 + 2126753390 cannot be represented in type 'int'

int M = L + (R - L) / 2
// This will prevent overflowing.
```

## Linked List

### Manipulation of head and tail in Linked List
```cpp
struct ListNode {

};

ListNode head, *tail = &head;
// Manipulate tail node here
return head.next;

// LeetCode - Merge Nodes In Between Zeros
```

### Reverse Linked List

```cpp
ListNode* reverseList(ListNode* head) {
    ListNode *prev = new ListNode();
    
    
    while(head) {
        auto node = head;
        head = head->next;
        node->next = prev->next;
        prev->next = node;
    }
    
    return prev->next;
}
```

## Priority Queue

### Priority Queue with Comparator
```cpp
auto cmp = [&](int a, int b){ return cnt[a] > cnt[b]; };
priority_queue<int, vector<int>, decltype(cmp)> pq(cmp);

// LeetCode - Merge K Sorted Lists
// LeetCode - Sort Characters By Frequency
```

### Priority Queue with Class Comparator
```cpp
class Cmp {
public:
    bool operator() (const pair<int, int>& a, const pair<int, int>& b) const {
        return a.second < b.second;
    }
};

priority_queue<pair<int, int>, vector<pair<int, int>>, Cmp> q(m.begin(), m.end()); // Assume there is an `m` storing pairs of `value, frequency`.
```

### Using Tuples in Priority Queue
```cpp
typedef tuple <int, int, int> Item;

priority_queue<Item, vector<Item>, greater<>> pq;

// Getting items from tuple
int ele = get<0>(pq.top());
int a = get<1>(pq.top());
int b = get<2>(pq.top());
```

## Vector

### Rotate Vector Left or right

```cpp
// Array - 1 2 3 4 5 6 7 8 9

// Rotate array to left by 3 positions.
// 4 5 6 7 8 9 1 2 3
rotate(vec1.begin(), vec1.begin() + 3, vec1.end());

// Rotate array to right by 3 positions.
// 7 8 9 1 2 3 4 5 6
rotate(vec1.begin(), vec1.begin() - 3, vec1.end());
```

### Find element in vector and replace it
```cpp
auto it = find (V.begin(), V.end(), num);
// it - V.begin() will given index of given num [0-indexed]
V[it - V.begin()] = otherNum;
```

### Slicing of Vector in C++

```cpp
vector<int> slicing(vector<int>& arr, int X, int Y){
    auto start = arr.begin() + X;
    auto end = arr.begin() + Y + 1;
    vector<int> result(Y - X + 1);
 
    copy(start, end, result.begin());
    return result;
}
```

### Erase Duplicates in Vector
```cpp
unorder_set<int> s;
for(int i : vec) {
    s.insert(i);
}

vec.assign(s.begin(), s.end());
sort(vec.begin(), vec.end());

Another Method: Slower than the above method

sort(vec.begin(), vec.end());
vec.erase(unique(vec.begin(), vec.end()), vec.end());
```

### Common Elements in Vector
```cpp
int main() {
	int countCommon = 0;
	int n = 6;
	vector<int> vec1 = {1, 3, 5, 7, 8, 9};
	int m = 7;
	vector<int> vec2 = {1, 2, 3, 7, 9, 4, 8};

	sort(vec1.begin(), vec1.end());
	sort(vec2.begin(), vec2.end());

	vector<int> v(vec1.size() + vec2.size());

	auto it = set_intersection(vec1.begin(), vec1.end(),vec2.begin(), vec2.end(),v.begin());

	cout << "Common Elements : " << it - v.begin() << "\n";
	cout << "The elements are : ";

	for ( auto st = v.begin(); st != it; ++st) {
		cout << *(st) << " ";
	}
}
```

## Dynamic Programming

### Longest Increasing Subsequence - LIS DP

```cpp
int LIS(vector<int> &a) {
    int n = a.size();
    vector<int> dp(n, 1e9);

    for(int i = 0; i < n; i++) {
        auto it = lower_bound(dp.begin(), dp.end(), a[i]);
        *it = a[i];
    }

    return lower_bound(dp.begin(), dp.end(), 1e9) - dp.begin();
}
```

### Partial Sum
```cpp

int N = A.size();
vector<int> pre(N + 1);
partial_sum(begin(A), end(A), begin(pre) + 1);
// Or simply
for (int i = 0; i < N; ++i) pre[i + 1] = pre[i] + A[i];

```

## Graphs

### Can We Go From Source To Destination
```cpp
vector<int> G[100];
vector<bool>seen;

void dfs(int v) {
    seen[v] = true;
    for (auto next_v : G[v]) { 
        if (seen[next_v]) continue;
        dfs(next_v);
    }
}

void solve() { 
    int N, M,s,t;
    cin >> N >> M >> s >> t;

    for (int i = 1; i <=M; ++i) {
        int a, b;
        cin >> a >> b;
        G[a].push_back(b);
    }

    seen.assign(100, false);
    dfs(s);

    if (seen[t]) {
        cout << "Yes" << endl;
    } else {
        cout << "No" << endl;
    }

}
```

### Print Euler Tour
```cpp

vector<int> adj[1000]; 
int vis[1000]; 
int Euler[2000]; 

void eulerTree(int u, int &indx)
{
    vis[u] = 1;
    Euler[indx++] = u;
    for (auto it : adj[u]) {
        if (!vis[it]) {
            eulerTree(it, indx);
            Euler[indx++] = u;
        }
    }
}
 
void printEulerTour(int root, int N)
{
    int index = 0;  
    eulerTree(root, index);
    for (int i = 0; i < (2*N-1); i++)
        cout << Euler[i] << " ";
}

void solve() {
    int n, m;
    cin >> n >> m;

    for(int i = 0; i < m; i++) {
        int , v;
        cin >> u >> v;
        adj[u].push_back(v);
        adj[v].push_back(u);
    }

    printEulerTour(1, n);
}
```

### Breadth First Search
```cpp
void bfs()
{
    int n, m;
    cin>> n >> m;
    vector<int> adj[n+1];
    memset(adj, 0, sizeof adj);

    for(int i = 0; i < m; i++)
    {
        int x, y;
        cin >> x >> y;
        adj[x].push_back(y);
        adj[y].push_back(x);
    }

    // Source Vertex
    int s = 1;
    
    queue<int> q;
    vector<bool> used(n+1);
    vector<int> d(n+1), p(n+1);

    q.push(s);
    used[s] = true;
    p[s] = -1;
    while (!q.empty()) {
        int v = q.front();
        q.pop();
        for (int u : adj[v]) {
            if (!used[u]) {
                used[u] = true;
                q.push(u);
                d[u] = d[v] + 1;
                p[u] = v;
            }
        }
    }

    // Check if there is any path between source vertex and vertex u.
    int u = 4;

    if (!used[u]) {
        cout << "No path!";
    } else {
        vector<int> path;
        for (int v = u; v != -1; v = p[v])
            path.push_back(v);
        reverse(path.begin(), path.end());
        cout << "Path: ";
        for (int v : path)
            cout << v << " ";
    }
}

// Problems
// LeetCode : 1971. Find if Path Exists in Graph
```
### DFS - First and Last Order
```cpp
vector<int> G[100];
vector<int> first_order;
vector<int> last_order;
vector<bool>seen;

void dfs(int v, int& first_ptr, int& last_ptr) {
    first_order[v] = first_ptr++;

    seen[v] = true; 
    for (auto next_v : G[v]) { 
        if (seen[next_v]) continue;
        dfs(next_v, first_ptr, last_ptr);
    }
    last_order[v] = last_ptr++;
}

void solve()
{ 
	int N, M; cin >> N >> M;

	for (int i = 1; i <=M; ++i) {
	    int a, b;
	    cin >> a >> b;
	    G[a].push_back(b);
	    G[b].push_back(a);
	}

	seen.assign(100, false);
	first_order.resize(100);
    last_order.resize(100);
	int first_ptr = 0, last_ptr = 0;
	dfs(0, first_ptr, last_ptr);

	for (int v = 0; v < N; ++v)
        cout << v << ": " << first_order[v] << ", " << last_order[v] << endl;
}
```
### Dijkstra's Algorithm
```cpp
const int N = 3e5 + 9;
int n, m;
vector<pair<int, int>> g[N];


// First parameter is source vertex and second is adjacency list
vector<long long> dijkstra(int s, vector<pair<int, int>> g[])
{
    priority_queue<pair<long long, int>, vector<pair<long long, int>>, greater<pair<long long, int>>> q;
    vector<long long> d(n + 1, 1e18); vector<bool> vis(n + 1, 0);
    q.push({0, s});
    d[s] = 0;
    while(!q.empty()){
        auto x = q.top(); q.pop();
        int u = x.second;
        if(vis[u]) continue; vis[u] = 1;
        for(auto y: g[u]){
            int v = y.first; long long w = y.second;
            if(d[u] + w < d[v]){
                d[v] = d[u] + w; q.push({d[v], v});
            }
        }
    }
    return d;
}

 
int u[N], v[N], w[N];
void solve()
{
	cin >> n >> m;
    for(int i = 1; i <= m; i++){
        cin >> u[i] >> v[i] >> w[i];
        g[u[i]].push_back({v[i], w[i]});
        g[v[i]].push_back({u[i], w[i]});
    }

    auto d1 = dijkstra(1, g);
    auto d2 = dijkstra(5, g);
    auto d3 = dijkstra(8, g);

    for(int i = 1; i <= n; i++) {
    	cout << d1[i] << " ";
    }
    cout << "\n";
    for(int i = 1; i <= n; i++) {
    	cout << d2[i] << " ";
    }
    cout << "\n";
    for(int i = 1; i <= n; i++) {
    	cout << d3[i] << " ";
    }
    cout << "\n";
}

// Input
// 8 13
// 1 2 2
// 1 3 9
// 2 3 7
// 2 4 8
// 3 5 3
// 4 5 2
// 5 6 1
// 1 7 3
// 7 8 2
// 8 5 3
// 7 6 6
// 8 3 2
// 1 8 8

// Output
// 0 2 7 10 8 9 3 5 
// 8 10 3 2 0 1 5 3 
// 5 7 2 5 3 4 2 0 
```
### Lowest Common Ancestor
```cpp
const int maxN = 2e5 + 1;
const int logN = 20;

int p[maxN][logN];
int timer, in[maxN], out[maxN];
vector<int> G[maxN];

void dfs(int u = 1, int par = 1) {
	in[u] = ++timer;
	p[u][0] = par;
	for(int i = 1; i < logN; i++) {
		p[u][i] = p[p[u][i-1]][i - 1];
	}
	for(int v: G[u]) {
		if(v != par) {
			dfs(v, u);
		}
	}
	out[u] = ++timer;
}

bool ancestor(int u, int v) {
	return in[u] <= in[v] && out[u] >= out[v];
}

int lca(int u, int v) {
	if(ancestor(u, v)) return u;
	if(ancestor(v, u)) return v;

	for(int i = logN - 1; i >= 0; i--) {
		if(!ancestor(p[u][i] , v)) {
			u = p[u][i];
		}
	}
	return p[u][0];
}

void solve()
{
	int N, M, Q, x, y, a, b;
	cin >> N >> M >> Q;
	for(int i = 2; i <= N; i++) {
		cin >> x >> y;
		G[x].push_back(y);
		G[y].push_back(x);
	}

	dfs();

	for(int q = 0; q < Q; q++) {
		cin >> a >> b;
		cout << lca(a, b) << "\n";
	}
}

// Input
// 11 10 4
// 1 2
// 2 3
// 3 4
// 3 5
// 4 6
// 4 7
// 5 9
// 2 8
// 8 10
// 8 11
// 11 6
// 7 9
// 4 9
// 6 7

// Output
// 2
// 3
// 3
// 4
```
### Number of Connected Components
```cpp
vector<int> G[100];

vector<bool> seen;
void dfs(int v) {
    seen[v] = true;
    for (auto next_v : G[v]) { 
        if (seen[next_v]) continue;
        dfs(next_v); 
    }
}


void solve()
{ 
    int N, M; cin >> N >> M;

    for (int i = 1; i <=M; ++i) {
        int a, b;
        cin >> a >> b;
        G[a].push_back(b);
        G[b].push_back(a);
    }

    int count = 0;
    seen.assign(100, false);
    for (int v = 1; v <=N; ++v) {
        if (seen[v]) continue; // Through if v has been searched
        dfs(v); // If v is unsearched, perform DFS starting from v
        ++count;
    }
    cout << count << endl;
}
```

### Kruskal Algorithm - Minimum Spanning Tree

```cpp
class UnionFind {
    vector<int> id;
    int size;
public:
    UnionFind(int N) : id(N), size(N) {
        iota(begin(id), end(id), 0);
    }
    int find(int a) {
        return id[a] == a ? a : (id[a] = find(id[a]));
    }
    void connect(int a, int b) {
        int p = find(a), q = find(b);
        if (p == q) return;
        id[p] = q;
        --size;
    }
    bool connected(int a, int b) {
        return find(a) == find(b);
    }
    int getSize() { return size; }
};
class Solution {
public:
    int minCostConnectPoints(vector<vector<int>>& A) {
        int N = A.size(), ans = 0;
        vector<array<int, 3>> E;
        for (int i = 0; i < N; ++i) {
            for (int j = i + 1; j < N; ++j) E.push_back({ abs(A[i][0] - A[j][0]) + abs(A[i][1] - A[j][1]), i, j });
        }
        make_heap(begin(E), end(E), greater<array<int, 3>>());
        UnionFind uf(N);
        while (uf.getSize() > 1) {
            pop_heap(begin(E), end(E), greater<array<int, 3>>());
            auto [w, u, v] = E.back();
            E.pop_back();
            if (uf.connected(u, v)) continue;
            uf.connect(u, v);
            ans += w;
        } 
        return ans;
    }
};
```

Problems
1. [Min Cost To Connect All Pairs](https://leetcode.com/problems/min-cost-to-connect-all-points/)
2. [Connecting Cities With Minimum Cost](https://leetcode.com/problems/connecting-cities-with-minimum-cost/)

### Euler path - Heirholzer Algorithm 
```cpp
// LeetCode Problem - Valid Arrangement of Pairs
vector<vector<int>> validArrangement(vector<vector<int>>& E) {
    int N = E.size();
    unordered_map<int, vector<int>> G;
    unordered_map<int, int> indegree, outdegree;
    G.reserve(N);
    indegree.reserve(N);
    outdegree.reserve(N);
    for (auto &e : E) {
        int u = e[0], v = e[1];
        outdegree[u]++;
        indegree[v]++;
        G[u].push_back(v);
    }
    int start = -1;
    for (auto &[u, vs] : G) {
        if (outdegree[u] - indegree[u] == 1) {
            start = u; // If there exists one node `u` that `outdegree[u] = indegree[u] + 1`, use `u` as the start node.
            break;
        }
    }
    if (start == -1) start = E[0][0]; // If there doesn't exist such node `u`, use any node as the start node
    vector<vector<int>> ans;
    function<void(int)> euler = [&](int u) {
        auto &vs = G[u];
        while (vs.size()) {
            int v = vs.back();
            vs.pop_back();
            euler(v);
            ans.push_back({ u, v }); // Post-order DFS. The edge is added after node `v` is exhausted
        }
    };
    euler(start);
    reverse(begin(ans), end(ans)); // Need to reverse the answer array in the end.
    return ans;
}
```

### Bipartite Graph
```cpp
bool isBipartite(vector<vector<int>>& G) {
    vector<int> id(G.size());
    function<bool(int, int)> dfs = [&](int u, int prev) {
        if (id[u]) return id[u] != prev; // This node's part should be the same as the part of the previous part
        id[u] = -prev; // Assign nodes to one of the two parts, -1 or 1
        for (int v : G[u]) {
            if (!dfs(v, id[u])) return false;
        }
        return true;
    };
    for (int i = 0; i < G.size(); ++i) {
        if (id[i]) continue; // This node is already assigned to a part
        if (!dfs(i, 1)) return false;
    }
    return true;
}
```

### Bellman Ford Algorithm
```cpp
vector<int> bellmanFord(vector<vector<int>>& edges, int V, int src) {
    vector<int> dist(N, INT_MAX);
    dist[src] = 0;
    for (int i = 1; i < V; ++i) { // try to use all the edges to relax for V-1 times.
        for (auto &e : edges) {
            int u = e[0], v = e[1], w = e[2];
            if (dist[u] == INT_MAX) continue;
            dist[v] = min(dist[v], dist[u] + w); // Try to use this edge to relax the cost of `v`.
        }
    }
    return dist;
}
```
## Recursion

### Maximum Digit in Number
```cpp
int maxDigitInNumber(int n) {
    if(n < 10) return n;
    return max( maxDigitInNumber(n / 10), n % 10);
}
```

## Binary Trees

### Find Path From Root To Target Node

```cpp
// It will store the path in vector passed to this function.
bool findPath(TreeNode *node, TreeNode *target, vector<TreeNode*> &path) {
    if (!node) return false;
    path.push_back(node);
    if (node == target) return true;
    if (findPath(node->left, target, path) || findPath(node->right, target, path)) return true;
    path.pop_back();
    return false;
}
```

## String

### stringstream Implementation
```cpp
stringstream ss;
ss << "Kiranpal Singh";

cout << ss.str() << "\n";

// We can also extract words from a string, perform some operation on each word 
stringstream ss(sentence);
string word, ans;
while(ss >> word) {
    ans += performOperation(word) + " ";
}

// https://leetcode.com/problems/apply-discount-to-prices/
```

### Convert Vector to Unordered Set
```cpp
vector<string> V = {"One", "Two", "Three", "Four", "Five"};
unordered_set<string> S(V.begin(), V.end());

// Use Cases
// -> To find any particular element : S.count("word");
// -> To erase any particular element : S.erase("word");

// 705 LeetCode - Design HashSet
```

### Euler Phi Function
```cpp
vector< int > euler_phi_table(int n) {
  vector< int > euler(n + 1);
  for(int i = 0; i <= n; i++) {
    euler[i] = i;
  }
  for(int i = 2; i <= n; i++) {
    if(euler[i] == i) {
      for(int j = i; j <= n; j += i) {
        euler[j] = euler[j] / i * (i - 1);
      }
    }
  }
  return euler;
}

template< typename T >
T euler_phi(T n) {
  T ret = n;
  for(T i = 2; i * i <= n; i++) {
    if(n % i == 0) {
      ret -= ret / i;
      while(n % i == 0) n /= i;
    }
  }
  if(n > 1) ret -= ret / n;
  return ret;
}

void EulerPhiDemo(int n) {
  int countPhi = 0;
  vector<int> whichNum;
  for(int i = 0; i <= n; i++) {
    if(gcd(i, n) == 1) {
      whichNum.push_back(i);
      countPhi++;
    }
  }
  cout << "Euler Phi of " << n << " : " << countPhi << "\n";
  cout << "The numbers are : ";
  for(auto &a: whichNum){
    cout << a << " ";
  }
  cout << "\n";
}

void solve()
{
	auto eulerTable = euler_phi_table(100);
	for(auto &a: eulerTable) {
		cout << a << " ";
	}
	cout << "\n";

	auto eulerNumber = euler_phi(20);
	cout << eulerNumber << "\n";

  EulerPhiDemo(5);
  EulerPhiDemo(11);
  EulerPhiDemo(20);
}

// Output
// Euler Phi Table
// 0 1 1 2 2 4 2 6 4 6 4 10 4 12 6 8 8
// 16 6 18 8 12 10 22 8 20 12 18 12 28
// 8 30 16 20 16 24 12 36 18 24 16 40
// 12 42 20 24 22 46 16 42 20 32 24 
// 52 18 40 24 36 28 58 16 60 30 36
// 32 48 20 66 32 44 24 70 24 72 36
// 40 36 60 24 78 32 54 40 82 24 64
// 42 56 40 88 24 72 44 60 46 72 32
// 96 42 60 40 

// Euler Phi Number
// 8

// Euler Phi Demo
// Euler Phi of 5 : 4
// The numbers are : 1 2 3 4 
// Euler Phi of 11 : 10
// The numbers are : 1 2 3 4 5 6 7 8 9 10 
// Euler Phi of 20 : 8
// The numbers are : 1 3 7 9 11 13 17 19 
```

### Finding if element inserted in set or not
```cpp
set<int> S;
int N = 6;
for(int i = 0; i < N; i++) {
    int x; cin >> x;
    if(S.insert(x).second) {
        cout << "New Element is inserted :)" << "\n";
    } else {
        cout << "Element already exists  :(" << "\n";
    }
}

// Input = 1 2 3 4 2 5
// Output: 
// New Element is inserted :)
// New Element is inserted :)
// New Element is inserted :)
// New Element is inserted :)
// Element already exists  :(
// New Element is inserted :)
```

## String Algorithm

### Rabin Karp Algorithm
```cpp
string s,t;
//t -> text s-> pattern

vector<int> rabin_karp(string const& s, string const& t) {
    const int p = 31; 
    const int m = 1e9 + 9;
    int S = s.size(), T = t.size();

    vector<long long> p_pow(max(S, T)); 
    p_pow[0] = 1; 
    for (int i = 1; i < (int)p_pow.size(); i++) 
        p_pow[i] = (p_pow[i-1] * p) % m;

    vector<long long> h(T + 1, 0); 
    for (int i = 0; i < T; i++)
        h[i+1] = (h[i] + (t[i] - 'a' + 1) * p_pow[i]) % m; 
    long long h_s = 0; 
    for (int i = 0; i < S; i++) 
        h_s = (h_s + (s[i] - 'a' + 1) * p_pow[i]) % m; 

    vector<int> occurences;
    for (int i = 0; i + S - 1 < T; i++) { 
        long long cur_h = (h[i+S] + m - h[i]) % m; 
        if (cur_h == h_s * p_pow[i] % m)
            occurences.push_back(i);
    }
    return occurences;
}

void solve()
{
    cin >> t >> s;
    ll n = s.length();

    // Prints the vector of indices where pattern is matched in text.
    auto a = rabin_karp(s, t);
    for(auto &ele: a) {
        cout << ele << " ";
    }
    cout << "\n";
}

//Input
// abcdeaabcfgabc abc
// Output
// 0 6 11
```
### Z Function - Prefix Function
```cpp
vector<int> z_function(string s) {
    int n = (int) s.length();
    vector<int> z(n);
    for (int i = 1, l = 0, r = 0; i < n; ++i) {
        if (i <= r)
            z[i] = min (r - i + 1, z[i - l]);
        while (i + z[i] < n && s[z[i]] == s[i + z[i]])
            ++z[i];
        if (i + z[i] - 1 > r)
            l = i, r = i + z[i] - 1;
    }
    return z;
}
```

### Adding numbers in string
```cpp
string addStr(const string& a, const string& b) {
	int as = (int)a.size() - 1;
	int bs = (int)b.size() - 1;
	string res;
	int carry = 0;
	for (int i = 0;; ++i) {
		int v = carry;
		carry = 0;
		if (i <= as) v += a[as-i] - '0';
		if (i <= bs) v += b[bs-i] - '0';
		if (v >= 10) {
			v -= 10;
			carry = 1;
		}
		if (i > as && i > bs && v == 0) break;
		res.push_back(v + '0');
	}
	reverse(res.begin(), res.end());
	return res;
}


void solve()
{
	string a, b;
	cin >> a >> b;

	string ans = addStr(a, b);
	cout << ans << "\n";
}

// Input
// 5555
// 4444

// Output
// 9999
```
### Longest Prefix Suffix
```cpp
// Longest prefix which is also suffix
// The prefix and suffix should not overlap
vector<int> computeLPS(string t) {
	int m = t.length();
    vector<int> lps(m);
 
    int i = 1, len = 0;
    lps[0] = 0;
 
    while (i < m) {
        if (t[i] == t[len]) {
            len++;
            lps[i] = len;
            i++;
        }
        else {
            if (len != 0) {
                len = lps[len - 1];
            }
            else {
                lps[i] = 0;
                i++;
            }
        }
    }
    return lps;
}

void solve()
{
	string a, b;
    cin >> a >> b;  

    auto A = computeLPS(a);
    auto B = computeLPS(b);

    for(auto &a: A) {
        cout << a << " ";
    }
    cout << "\n";

    for(auto &b: B) {
        cout << b << " ";
    }
    cout << "\n";
}

// Input
// abcdabcdabcd
// abcdefabcdefabcdef
// Output
// 0 0 0 0 1 2 3 4 5 6 7 8 
// 0 0 0 0 0 0 1 2 3 4 5 6 7 8 9 10 11 12 

```

## Lambda Function

### Definition of Lambda Function
```cpp
// Void Lambda Function
function<void(int, int)> dfs = [&](int start, int goal) {
    // Write your code here.          
};
```

### Lambda Function to Check if Vector is Permutation 
```cpp
int n = 6;
auto isPermutation = [&](const vector<int> &A)->bool{
    vector<int> vis(n + 1, false);
    for(auto x : A){
        if(x <= 0 || x > n || vis[x])
            return false;
        vis[x] = true;
    }
    return true;
};

vector<int> A = {1, 2, 3, 4, 5, 1};
vector<int> B = {3, 4, 5, 6, 1, 2};

if(isPermutation(A)) {
    cout << "Vector A is permutation" << "\n";
}
if(isPermutation(B)) {
    cout << "Vector B is permutation" << "\n";
}
```

## Heaps

### Max Heap and Min Heap
```cpp
// Minimum heap and Maximum heap
void solve()
{
	priority_queue<int, vector<int>, greater<int> > minHeap;
	priority_queue<int, vector<int> > maxHeap;

	int n, x;
	cin >> n;
	for(int i = 0; i < n; i++) {
		cin >> x;
		minHeap.push(x);
		maxHeap.push(x);
	}

	auto a = minHeap;
	while(!a.empty()) {
		cout << a.top() << " ";
		a.pop();
	}
	cout << "\n";

	auto b = maxHeap;
	while(!b.empty()) {
		cout << b.top() << " ";
		b.pop();
	}
	cout << "\n";
}

// Input
// 8
// 1 5 2 19 23 9 7 33
// Output
// 1 2 5 7 9 19 23 33 
// 33 23 19 9 7 5 2 1 
```

### Convert Vector to Heaps in C++

```cpp
vector<array<int, 3>> E;

make_heap(begin(E), end(E), greater<array<int, 3>>());
pop_heap(begin(E), end(E), greater<array<int, 3>>());

// Now the smallest element in Heap is at the back of vector E.
auto [w, u, v] = E.back();
E.pop_back()
```

Problems
1. [Min Cost To Connect All Pairs](https://leetcode.com/problems/min-cost-to-connect-all-points/)

## Permutation

### Next Permutation
```cpp
void solve()
{
	string s;
	cin >> s;
	sort(s.begin(), s.end());

	do {
		cout << s << "\n";
	} while(next_permutation(s.begin(), s.end()));
}

// Input
// abcd

// Ouput
// abcd
// abdc
// acbd
// acdb
// adbc
// adcb
// bacd
// badc
// bcad
// bcda
// bdac
// bdca
// cabd
// cadb
// cbad
// cbda
// cdab
// cdba
// dabc
// dacb
// dbac
// dbca
// dcab
// dcba
```

## Mathematics

### Chicken McNugget Theorem
```cpp
/* The Chicken McNugget Theorem states that for any two relatively prime positive
integers m and n, the greatest integer that cannot that cannot be written
in the form a*m + b *n for non-negative integers a, b is mn - m - n.  */

bool chickenMcNuggetTheorem(int m, int n, int number) {
	for(int i = 0; i <= 10; i++) {
		int y = number - i * n;
		if(y >= 0 && y % m == 0) {
			return true;
		}	
	}
	return false;
}

bool chickenMcNuggetTheoremModified(int m, int n, int number) {
	if(number >= n * (number % m)) {
		return true;
	} else {
		return false;
	}
}

void solve()
{
	int t, n;
	cin >> t;
	while(t--) {
		cin >> n;
		if(chickenMcNuggetTheoremModified(11, 111, n)) {
			cout << "YES" << "\n";
		} else {
			cout << "NO" << "\n";
		}
	}
}

// Input
// 3
// 33
// 144
// 69

// Output
// YES
// YES
// NO

```
### Sum of Two Numbers with Given Base
```cpp
// Returns sum of two numbers a and b with given base 
int sumWithBase(string a, string b, int base)
{
    int len_a, len_b;
 
    len_a = a.size(); len_b = b.size();
 
    string sum, s;
    s = "";
    sum = "";
 
    int diff;
    diff = abs(len_a - len_b);
 
    for (int i = 1; i <= diff; i++) s += "0";
 
    if (len_a < len_b) a = s + a;
    else b = s + b;
 
    int curr, carry = 0;
 
    for (int i = max(len_a, len_b) - 1; i > -1; i--) 
    {
        curr = carry + (a[i] - '0') + (b[i] - '0');
        carry = curr / base;
        curr = curr % base;
        sum = (char)(curr + '0') + sum;
    }

    if (carry > 0) sum = (char)(carry + '0') + sum;
    
    int ans = stoi(sum);
    return ans;
}

void solve()
{
    string a, b;
    cin >> a >> b;
    cout << sumABwithBase(a, b, 10);
}

// Input
// 11 12
// Output
// 23
```
## Prime Numbers

### Prime Numbers in Range
```cpp
const ll MAXN = 1e7;
bool comp[MAXN + 10];
vector<ll> primeVec;

void sieveOfEratosthenes()
{
   for(int i = 2; i <= MAXN; i++){
        if(comp[i]) continue;
        primeVec.pb(i);        
        for(int j = 2 * i; j <= MAXN; j += i){
            comp[j] = true;
        }
    }
}

int L,R;

void solve()
{
    // Implementation
    sieveOfEratosthenes();
    cin >> L >> R;
    // For finding prime numbers in range L,R
    ll rangeAns = (upper_bound(primeVec.begin(), primeVec.end(), R)
                 - upper_bound(primeVec.begin(), primeVec.end(), L));

    cout << rangeAns;
}

// Input - > 1 100
// Output -> 25 (25 Prime numbers between 2 and 100 inclusive)
```
## Base Conversion

### Convert To Decimal From Base K
```cpp

int convertToDecimal(string s, int k) {
  int ans = 0;
  for(char x: s) {
    ans *= k;
    ans += x - '0';
  } return ans;
}

int main(){
    int k;
    string a,b;
    cin >> k >> a >> b;
    int A = convertToDecimal(a, k);
    int B = convertToDecimal(b, k);
    cout << A*B << endl;
    return 0;
}
```

## GCD and LCM

### Maximum GCD in range [L, R]
```cpp
// Finding maximum gcd of two numbers a and b in range [L, R]
// in O(n) time instead of O(n ^ 2) time.
	// cin >> L >> R;
int maxGCD = -1e9;
int operations = 0;

for(int i = L; i <= R; i++) {
	for(int j = i + 1; j <= R; j++) {
		maxGCD = max(maxGCD, int(gcd(i, j)));
		operations++;
	}
}

cout << maxGCD << "\n";
int modifiedOperations = 0;

for(int c = R; c > 0; c--) {
	modifiedOperations++;
	if((L + c - 1) / c < R / c) {
		cout << c << "\n";
		goto end;
	}
}
end:;

cout << operations << "\n";
cout << modifiedOperations << "\n";

// Input
// 100 279
// Output
// 139
// 139
// 16110
// 141
```

### Dirichlet's Convolution

```cpp
namespace Dirichlet {
  const int T = 1e6 + 9;
  long long phi[T];
  gp_hash_table<long long, long long> mp;
  long long dp[T], inv;
  int sz, spf[T], prime[T];
  void init() {
      memset(spf, 0, sizeof spf);
      phi[1] = 1; sz = 0;
      for (int i = 2; i < T; i++) {
          if (spf[i] == 0) phi[i] = i - 1, spf[i] = i, prime[sz++] = i;
          for (int j = 0; j < sz && i * prime[j] < T && prime[j] <= spf[i]; j++) {
              spf[i * prime[j]] = prime[j];
              if (i % prime[j] == 0) phi[i * prime[j]] = phi[i] * prime[j];
              else phi[i * prime[j]] = phi[i] * (prime[j] - 1);
          }
      }
      dp[0] = 0;
      for(int i = 1; i < T; i++) dp[i] = dp[i - 1] + phi[i];
      inv = 1; // g(1)
  }
  long long p_c(long long n) {
      if (n % 2 == 0) return n / 2 * ((n + 1));
      return (n + 1) / 2 * (n);
  }
  long long p_g(long long n) {
      return n;
  }
  long long solve (long long x) {
      if (x < T) return dp[x];
      if (mp.find(x) != mp.end()) return mp[x];
      long long ans = 0;
      for (long long i = 2, last; i <= x; i = last + 1) {
          last = x / (x / i);
          ans += solve (x / i) * (p_g(last) - p_g(i - 1));
      }
      ans = p_c(x) - ans;
      ans /= inv;
      return mp[x] = ans;
  }
}

// Find number of pairs (a, b) such that a <= b <= N and gcd(a, B) = X

int main() {
    int n, x; cin >> n >> x;
    cout << solve(n / x) << '\n';
}
```

### Euler Totient Function

```cpp
#define int long long
#define maxn 1500001
int phi[maxn];
int s_phi[maxn];
void pre()
{
    int i,j;
    for(i=1;i<maxn;i++)
        phi[i] = i;
    s_phi[1] = 1;
    for(i=2;i<maxn;i++)
    {
        if(phi[i] == i)
        {
            for(j=i;j<maxn;j=j+i)
                phi[j] = (phi[j]/i)*(i-1);
        }
        s_phi[i] = s_phi[i-1] + phi[i];    
    }
}
int func(int n)
{
    if(n < maxn)
       return s_phi[n]; 
    int g;
    int x = sqrt(n);
    int sum = 0;
    for(g=2;g<=x;g++)
    {
        sum = sum + func(n/g);
    }
    x = n/(x+1);
    for(g=1;g<=x;g++)
        sum = sum + s_phi[g]*(n/g - n/(g+1));
    sum = n*(n+1)/2 - sum;
    return sum;    
}

// Find number of pairs (a, b) such that a <= b <= N and gcd(a, B) = X

signed main() {
    ios_base::sync_with_stdio(false);
    cin.tie(0);
    int t = 1;
    pre();
    //cin >> t;
    while(t--){
        int N, X;
        cin >> N >> X;
        cout << func(N/X);
    }
}
```

## Geometry

### Point Structure in Geometry
```cpp
typedef double T;
struct pt {
	T x, y;
	pt operator+ (pt p) {
		return {x + p.x, y + p.y};
	}

	pt operator- (pt p) {
		return {x - p.x, y - p.y};
	}

	pt operator* (T d) {
		return { x * d, y * d};
	}

	pt operator/ (T d) {
		return {x/d, y/d};
	}
};

bool operator==(pt a, pt b) {
	return a.x == b.x && a.y == b.y;
}

bool operator!= (pt a, pt b) {
	return !(a == b);
}

T sq(pt p) {
	return p.x * p.x + p.y * p.y;
}

double abs(pt p) {
	return sqrt(sq(p));
}

ostream& operator<< (ostream& os, pt p) {
	return os << "(" << p.x << "," << p.y << ")";
}

void solve()
{
    pt a, b;
    cin >> a.x >> a.y >> b.x >> b.y;
    cout << a+b << " " << a-b << "\n"; 
    cout << a*-1 << " " << b/2 << "\n"; 

    pt c;
    cin >> c.x >> c.y;
    cout << abs(c) << "\n";
}

// Input
// 3 4
// 2 -1
// -5 -10

// Output
// (5,3) (1,5)
// (-3,-4) (1,-0.5)
// 11.1803

```

## Mathematical Equations

### Find x and y in a.x + b.y = N

```cpp
void equation(int a, int b, int n) {
    for (int i = 0; i * a <= n; i++) {
        if ((n - (i * a)) % b == 0) {
            cout << "x = " << i << ", y = " << (n - (i * a)) / b;
            return;
        }
    }
    cout << "No solution exists." << "\n";
}
```

## Miscellaneous

### Numeric Limits
```cpp
long long a = numeric_limits<long long>::max();
int b = numeric_limits<int>::max();
```

### Median of an array

```cpp
int median(vector<int> &A) {
	sort(A.begin(), A.end());
	int N = A.size();

	cout << "Size : " << N << "\n"; 

	for(auto a : A) {
			cout << a << " ";
	}
	cout << "\n";

	if(N % 2 == 0) {
		return A[(N - 2) / 2];
	}

	return A[(N - 1) / 2];
}
```

### Reverse a number

```cpp
int rev(int n) {
  string s = to_string(n);
  reverse(s.begin(), s.end());
  
  return stoi(s);
}

int rev2(int x) {
    int b = 0;
    while (a > 0) {
        b = b * 10 + (a % 10);
        a /= 10;
    }
    return b;
}

int main() 
{
    int n = 988;
    int m = 930;
    
    cout << rev(n) << "\n";
    cout << rev(m) << "\n";
}
```

### Generating Random Numbers in Range
```cpp
mt19937 rng{random_device{}()};
uniform_real_distribution<double> uni{0, 1};
// It will generate the random numbers every time in given range
// cout << uni(rng) << "\n";
```

<p align="left"> <img src="https://komarev.com/ghpvc/?username=kiranpalsingh1806&label=Views&color=blue&style=plastic" alt="kiranpalsingh" /> </p>
