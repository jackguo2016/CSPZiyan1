# Graph Coloring Solver: A Constraint Satisfaction Problem Approach

## Project Overview
This Java-based implementation tackles the Graph Coloring Problem, a classic NP-hard optimization challenge in computer science and operations research. The solver utilizes advanced constraint satisfaction techniques to efficiently color the vertices of a graph such that no two adjacent vertices share the same color, while minimizing the number of colors used.

## Key Features
- Efficient graph representation using adjacency lists for optimal memory usage and fast neighbor access.
- Implementation of the AC-3 (Arc Consistency Algorithm #3) for constraint propagation, enhancing the efficiency of the solving process.
- Integration of heuristic methods:
  - Minimum Remaining Values (MRV) for intelligent variable ordering.
  - Least Constraining Value (LCV) for dynamic value selection.
- Flexible input system allowing for various graph structures through a standardized file format.

## Algorithmic Components
1. **AC-3 Algorithm**: Implements arc consistency to reduce the domains of variables before and during the search process, significantly pruning the search space.
2. **MRV Heuristic**: Selects the variable with the fewest remaining values in its domain, effectively minimizing branching factor in the search tree.
3. **LCV Heuristic**: Chooses the least constraining value for each variable assignment, maximizing future solving flexibility.

## File Structure
- `Main.java`: Orchestrates the solving process, including file I/O, graph construction, and algorithm execution.
- `Node.java`: Encapsulates the vertex data structure, managing adjacency information and color assignments.
- `test.txt`: Sample input file demonstrating the required format for graph specification.

## Usage Instructions
1. Prepare an input file following the format specified in `test.txt`.
2. Execute `Main.java` to initiate the solving process.
3. The program constructs the graph representation from the input file.
4. (To be implemented) The solver applies AC-3, MRV, and LCV to determine an optimal coloring.

## Implementation Details
- Graph Construction: O(E) time complexity, where E is the number of edges.
- AC-3 Algorithm: Worst-case time complexity of O(ed³), where e is the number of arcs and d is the size of the largest domain.
- MRV and LCV: Implemented as comparator functions for priority queue-based variable and value selection.

## Future Enhancements
- Complete implementation of the AC-3 algorithm for constraint propagation.
- Integration of MRV and LCV heuristics into the main solving loop.
- Development of a backtracking search algorithm leveraging the implemented heuristics.
- Performance analysis and optimization for large-scale graphs.

## Author
Ziyan

## Academic References
1. Mackworth, A. K. (1977). Consistency in networks of relations. Artificial Intelligence, 8(1), 99-118.
2. Russell, S. J., & Norvig, P. (2010). Artificial Intelligence: A Modern Approach (3rd ed.). Pearson Education.
3. Kumar, V. (1992). Algorithms for constraint-satisfaction problems: A survey. AI Magazine, 13(1), 32-44.


# Graph Coloring Solver

## 项目概述
这是一个用Java实现的图着色问题求解器。图着色问题是约束满足问题（CSP）的一个经典应用，目标是使用最少的颜色为图的所有顶点着色，同时确保相邻顶点的颜色不同。

## 功能特点
- 从文本文件读取图结构和可用颜色数量
- 使用邻接表表示图结构
- 实现AC3（弧一致性）算法进行约束传播
- 使用最小剩余值（MRV）和最少约束值（LCV）启发式方法优化求解过程

## 文件结构
- `Main.java`: 主程序逻辑，负责文件读取和图构建
- `Node.java`: 定义图中节点的结构和属性
- `test.txt`: 输入文件，包含图结构和颜色数量

## 使用方法
1. 准备输入文件（格式参考 `test.txt`）
2. 运行 `Main.java`
3. 程序将读取输入文件并构建图结构
4. （待实现）使用AC3算法和启发式方法求解图着色问题

## 待完成功能
- AC3算法的完整实现
- MRV和LCV启发式方法的实现
- 完整的图着色解决方案输出

## 作者
Ziyan Guo


