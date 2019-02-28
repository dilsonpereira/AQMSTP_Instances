# Instances for the Adjacent Only Quadratic Minimum Spanning Tree Problem

Instances are in the same format as QMSTP instances found in the literature.

Sample file:
```
param n := 3 ;
param m := 3 ;
set Edges := (1,2) (2,3) (1,3) ;
param c := [1,2] 4 [2,3] 9 [1,3] 0 ;
param q := [1,2,2,3] 1 [2,3,1,2] 1 [1,2,1,3] 5 [1,3,1,2] 5 [2,3,1,3] 6 [1,3,2,3] 6 ;
end;
```

In this example, the graph has n=3 vertices and m=3 edges.

Section `set Edges := (1,2) (2,3) (1,3) ; ` indicates the set of edges. Each edge is given in the format `(u, v)`, where `u` and `v` are the endpoints.

Section `param c := [1,2] 4 [2,3] 9 [1,3] 0 ;` indicates the edge costs. Each entry is in the format `[u, v] c`, where `u` and `v` are the endpoints and `c` is the cost.

Section `param q := [1,2,2,3] 1 [2,3,1,2] 1 [1,2,1,3] 5 [1,3,1,2] 5 [2,3,1,3] 6 [1,3,2,3] 6 ;` gives the quadratic costs. Each entry has the format `[u, v, w, x]`, where `(u,v)` corresponds to the first edge, `(w, x)` to the second, and `q` is their interaction cost. If `[u, v, w, x]` is given, `[w, x, u, v]` will also be given. The total cost is the sum of the costs given in the two entries.
