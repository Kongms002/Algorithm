# 위상 정렬 (Topological Sort)

### When?
순서가 정해져 있는 작업을 차례로 수행해야 할 때 사용한다.

### Condition
(1) DAG(Directed Acyclic Graph)에서만 적용이 가능
(2) 답이 여러개 존재할 수 있다.

## Pseudo Code
```
graph = [[]]
indegree = []
result = []

void topologicalSort():
  queue q;
  // 진입차수가 0인 노드를 큐에 삽입한다.
  for i->0 to n-1:
    if indegree[i] is 0:
      q.push(i);
  
  // 차례대로 노드 방문
  while !q.empty():
    nowNode<-q.front(); q.pop();
    
    result.push_back(nowNode);
    
    for i->0 to graph[nowNode].size():
      nextNode <- graph[nowNode][i];
      indegree[nextNode]--;
      
      if(indegree[nextNode] == 0)
        q.push(nextNode);
      
  for v in result:
     print(v);
```
