# assignment2-GANDRA
# ALEKHYA GANDRA
###### India
**India** is my favourite location. It is known for being the most populus **democractic** country.

---

## Directions to my favourite place
1. Take a safe ride from marryville to kansas.
2. Board a plane in Kansas Airport to Chicago.
3. Fly from Chicago to India for a long time.
4. After reaching india , we have a multiple ways of transport to reach destination place.
    1. Flights
    2. Trains
    3. Cars
    4. Three Wheelers
5. I mostly use Cars in India to reach my favourite place Warangal
6. Things I get with me for maximum enjoyment.
    * Novels
    * Playing Cards
    * Food

[Link to AboutMe](AboutMe.md) 

---

# FOOD TABLE

The following table describes famous food items that someone should try
| Name | Location | Cost |
| --- | --- | --- |
| Jilebhi | Karimnagar| $40 |
| Pani Puri | Warangal| $20 |
| putharekhulu | Bhimavaram| $60|


---
# PITHY QUOTES

> Life is what happens when you're busy making other plans. -*John Lennon*

>  When you reach the end of your rope, tie a knot in it and hang on. -*Franklin D. Roosevelt*

---

# CODE FENCING

>A Bipartite Graph is a graph whose vertices can be divided into two independent sets, U and V such that every edge (u, v) either connects a vertex from U to V or a vertex from V to U. In other words, for every edge (u, v), either u belongs to U and v to V, or u belongs to V and v to U. We can also say that there is no edge that connects vertices of same set.

[Link to Bipartite](https://www.geeksforgeeks.org/bipartite-graph/)


```
int n;
vector<vector<int>> adj;

vector<int> side(n, -1);
bool is_bipartite = true;
queue<int> q;
for (int st = 0; st < n; ++st) {
    if (side[st] == -1) {
        q.push(st);
        side[st] = 0;
        while (!q.empty()) {
            int v = q.front();
            q.pop();
            for (int u : adj[v]) {
                if (side[u] == -1) {
                    side[u] = side[v] ^ 1;
                    q.push(u);
                } else {
                    is_bipartite &= side[u] != side[v];
                }
            }
        }
    }
}

cout << (is_bipartite ? "YES" : "NO") << endl;

```

[Link to Source Code](https://cp-algorithms.com/graph/bipartite-check.html)