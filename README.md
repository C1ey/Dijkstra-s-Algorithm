# Dijkstra-s-Algorithm
A brief Introduction to Dijkstra's Algorithm (Including a short video)
Dijkstra's Algorithm is a popular algorithm in computer science used to find the shortest path between nodes in a graph, particularly in weighted graphs where each edge has a non-negative weight. The algorithm was conceived by Dutch computer scientist Edsger W. Dijkstra in 1956.

Here's an overview of how Dijkstra's Algorithm works:

1. **Initialization**: Start with a source node and assign it a distance of 0. Set the distance of all other nodes to infinity. Keep track of the shortest known distance from the source node to each node in the graph.

2. **Priority Queue**: Maintain a priority queue (often implemented using a min-heap) to keep track of nodes whose shortest distance from the source node is known but not yet finalized. Initially, the priority queue contains only the source node.

3. **Relaxation**: Repeat the following steps until the priority queue is empty:
   - Remove the node with the smallest known distance from the priority queue. This node is considered "finalized."
   - For each neighboring node of the removed node that has not been finalized:
     - Calculate the distance from the source node to the neighboring node through the removed node.
     - If this distance is shorter than the current shortest distance recorded for the neighboring node, update the shortest distance and update the priority queue accordingly.

4. **Termination**: When the priority queue is empty, the algorithm has found the shortest path from the source node to all other nodes in the graph.

5. **Path Reconstruction (Optional)**: If needed, the shortest path from the source node to any other node in the graph can be reconstructed by backtracking from the destination node to the source node, using the information stored during the algorithm's execution.

Dijkstra's Algorithm is guaranteed to find the shortest path from the source node to all other nodes in the graph, as long as the graph does not contain negative-weight edges. If negative-weight edges are present, a different algorithm, such as the Bellman-Ford algorithm, should be used.
