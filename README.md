# assingment2-shaik
# ZABHEEN #
####  Pizza hut
Economical on pocket and a great deal. ***Its is one of my favourites***. Dominos pizza is great along with the cold coffee beverage,cake. A great place to meet up frens chill out and have fun.



## Route to Airport
1.Gannavaram Airport is the nearest airport  
2.Head southwest on NH16 toward Old Airport Rd/Vijayawada Airport Rd  
3.Pass by Sai Baba Temple (on the left in 11.6 km) 
4.Continue straight to stay on NH16  
5.Pass by Samyuktha Vedika (on the left)  
6.At Benz Cir, take the 3rd exit onto MG Rd/Vijayawada Rd/Vijayawada - Machilipatnam Rd  
7.Pass by the gas station (on the left)  
8.Make a U-turn Pass by the gas station (on the right)Destination will be on the left  


### Food Iteams 
* Chicken sweetcorn Pizza
* Chicken Pizza
* wings Pizza
* veggies Pizza
* Stuffed Crush
* choco lava
* tastermaker
    
About Me
    https://github.com/zabheenshaik/assingment2-shaik/blob/main/Aboutme.md

## Sports
Table express the  sports data activity cost effectiveness data which was held on different location in our country and in the year-2020. Data indicates detailed cost analysis basket ball event held on area cost, is higher than badminton sports event, cricket is one of the best game in the world.

| SPORTS/ACTIVITY | LOCATION | AMOUNT |
| ------------- | ------------- | -------- |
| BASKETBALL | AMERICA | $4500 |
| BADMINTON | AUSTRALIA | $3200 |
| CRICKET | INDIA | $5500 |


## Qutoes
> You have to dream before your dreams can come true 
*- APJ Abdul Kalam*

> Never let the fear of striking out keep you from playing the game
*- Bade Ruth*

## Algorithim

>Graphs flows
A flow graph is a form of digraph associated with a set of linear algebraic or differential equations
A signal flow graph is a network of nodes (or points) interconnected by directed branches, representing a set of linear algebraic equations. The nodes in a flow graph are used to represent the variables, or parameters, and the connecting branches represent the coefficients relating these variables to one another. The flow graph is associated with a number of simple rules which enable every possible solution to be obtained.

>For more references : https://en.wikipedia.org/wiki/Flow_graph_(mathematics)

```ruby
 vector<int> parent, rank;

void make_set(int v) {
    parent[v] = v;
    rank[v] = 0;
}

int find_set(int v) {
    if (v == parent[v])
        return v;
    return parent[v] = find_set(parent[v]);
}

void union_sets(int a, int b) {
    a = find_set(a);
    b = find_set(b);
    if (a != b) {
        if (rank[a] < rank[b])
            swap(a, b);
        parent[b] = a;
        if (rank[a] == rank[b])
            rank[a]++;
    }
}

struct Edge {
    int u, v, weight;
    bool operator<(Edge const& other) {
        return weight < other.weight;
    }
};

int n;
vector<Edge> edges;

int cost = 0;
vector<Edge> result;
parent.resize(n);
rank.resize(n);
for (int i = 0; i < n; i++)
    make_set(i);

sort(edges.begin(), edges.end());

for (Edge e : edges) {
    if (find_set(e.u) != find_set(e.v)) {
        cost += e.weight;
        result.push_back(e);
        union_sets(e.u, e.v);
    }
}
```


>Competitive Programming Algorithim https://cp-algorithms.com/graph/mst_kruskal_with_dsu.html