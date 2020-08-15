# FordFolkerson Algorithm

[Click for Live Demo](https://mrganji9.github.io/Ford-Folkerson/)



> Ford-Fulkerson Algorithm for Maximum Flow Problem

## Introduction

*When a Graph Represent a Flow Network where every edge has a capacity. Also given that two vertices, source 's' and sink 't' in the graph, we can find the maximum possible flow from s to t with having following constraints:*

1. Flow on an edge doesn't exceed the given edge capacity
2. Incoming flow is equal to Outgoing flow for every vertex excluding sink and source

## Algorithm

1. Start with f(e) = 0 for all edge e ∈ E.
2. Find an augmenting path P in the residual graph Gf .
3. Augment flow along path P.
4. Repeat until you get stuck.

## Example

*Consider the following graph*

<img src="/AdvancedAlgorithms/VI Graph Algorithms/26 Maximum Flow/Ford-Folkerson/images/ford_fulkerson11.png">

*Maximum possible flow in the given graph is 23*

<img src="/AdvancedAlgorithms/VI Graph Algorithms/26 Maximum Flow/Ford-Folkerson/images/ford_fulkerson2.png">

> graph definition in my js code
```javascript
const graphs = 
  {
    nodes: {
      "s": { id: 's', label: 'S'},
      "a": { id: 'a', label: 'A'},
      "b": { id: 'b', label: 'B'},
      "c": { id: 'c', label: 'C'},
      "d": { id: 'd', label: 'D'},
      "t": { id: 't', label: 'T'}
    },
    edges: {
      "0": { id: "0", from:"s", to:"a",  capacity:20,  label:"0/20", },
      "1": { id: "1", from:"s", to:"c",  capacity:30,  label:"0/30", },
      "2": { id: "2", from:"a", to:"b",  capacity:10,  label:"0/10", },
      "3": { id: "3", from:"a", to:"d",  capacity:20,  label:"0/20", },
      "4": { id: "4", from:"b", to:"t",  capacity:15,  label:"0/15", },
      "5": { id: "5", from:"c", to:"b",  capacity:20,  label:"0/20", },
      "6": { id: "6", from:"d", to:"t",  capacity:30,  label:"0/30", }
    }
  };

```

**Arguments:**
- `graph`: The Graph which representing the flow network
- `nodes`: Graph nodes
- `edges`: Graph edge

**Returns:** Returns a number representing the maximum flow.
