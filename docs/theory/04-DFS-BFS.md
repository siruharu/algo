# DFS/BFS

## DFS
- 깊게 먼저 탐색
- 재귀 또는 스택 사용
- 경로 탐색/조합 문제에서 자주 사용

## BFS
- 가까운 것부터 탐색
- 큐 사용
- 최단 거리(간선 가중치 동일)에서 강력

## BFS 기본형
```python
from collections import deque

def bfs(start, graph):
    q = deque([start])
    visited = set([start])
    while q:
        cur = q.popleft()
        for nxt in graph[cur]:
            if nxt in visited:
                continue
            visited.add(nxt)
            q.append(nxt)
```

## 실수 포인트
- 방문 처리 시점 오류(큐에 넣을 때 방문 처리 권장)
- 2차원 배열에서 범위 체크 누락
