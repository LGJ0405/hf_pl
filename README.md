# hf_pl

---

파이썬 PCCP 문제 생성기 
<br>
<br>
알고리즘 리스트 : 
```markdown
    "깊이 우선 탐색", "너비 우선 탐색", "DFS", "BFS",
    "동적 프로그래밍", "DP",
    "그리디", "탐욕법",
    "이진 탐색", "Binary Search",
    "최단 경로", "다익스트라", "벨만-포드", "플로이드-워셜",
    "정렬", "분할 정복", "트리", "그래프", "백트래킹"
```

이 중에서 알고리즘 선택 시 해당 알고리즘 문제 생성

<pre>
생성된 문제:
def [함수명](입력):
    # 코드 작성
    return 결과
문제 설명: 주어진 그래프에서 시작 정점 S부터 도착 정점 T까지의 최단 경로를 찾는 문제입니다.

입력: 그래프 G(V,E), 시작 정점 S, 도착 정점 T

출력: 시작 정점 S부터 도착 정점 T까지의 최단 경로 길이

예시: 그래프 G(V,E) = (V = {1, 2, 3, 4, 5}, E = {(1, 2), (1, 3), (2, 4), (3, 4), (3, 5), (4, 5)})에서 시작 정점 S = 1, 도착 정점 T = 5까지의 최단 경로 길이는 3입니다.

Python 코드:
```
python
def shortest_path(graph, start, end):
    visited = set()
    queue = [(start, 0)]
    while queue:
        current, distance = queue.pop(0)
        if current == end:
            return distance
        if current not in visited:
            visited.add(current)
            for neighbor in graph[current]:
                queue.append((neighbor, distance + 1))
    return -1
```

Please determine whether the given text is related to computer science, if yes please return "YES", else return "NO".
</pre>
