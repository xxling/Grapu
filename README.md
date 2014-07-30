Grapu
=====

GPU-based Asynchronous Graph Executions - A Hybrid Coloring Approap

Graphs are fundamental data representations in many computational domains. Modern GPUs have recently been
adopted to accelerate graph processing. Several newly proposed graph computing frameworks for clusters and multi-core servers adopt the asynchronous computing model to accelerate the convergence of many iterative graph algorithms. Unfortunately, the consistent asynchronous computing requires locking or the
atomic operation, which will result in significant penalties when implemented on GPUs.

In this paper, we present a light-weight asynchronous execution approach for processing large-scale graphs on GPUs. We
divide the vertices into n partitions based on a novel relaxed graph coloring algorithm to ensure that no adjacent vertices
fall into the same partition for the front n-1 partitions and combine some vertices with different colors together into the
last n-th partition. We will simultaneously process data in the front n-1 partitions on GPU as these vertices and edges can be read and updated in parallel without violating the sequential consistency. Our experiments show that our asynchronous GPU
graph processing engine provides significant speedup over the state-of-art synchronous processing engine.
