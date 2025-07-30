---
type:
  - algorithm
---

### <span style="color:#ff8800"> algorithm:: Depth-first Search</span>
**procedure** DFS(_G_, _v_) **is**
    label _v_ as discovered
    **for all** directed edges from _v_ to _w that are_ **in** _G_.adjacentEdges(_v_) **do**
        **if** vertex _w_ is not labeled as discovered **then**
            recursively call DFS(_G_, _w_)


### <span style="color:#ffff00">algorithm:: Backtracking</span> 
Funktion FindeLösung (Stufe, Vektor)
  1. wiederhole, solange es noch neue Teil-Lösungsschritte gibt:
     a) wähle einen neuen Teil-Lösungsschritt;
     b) falls Wahl gültig ist:
               I) erweitere Vektor um Wahl;
              II) falls Vektor vollständig ist, return true; // Lösung gefunden!
        sonst:
                  falls (FindeLösung(Stufe+1, Vektor)) return true; // Lösung!
                  sonst mache Wahl rückgängig; // Sackgasse (Backtracking)!
  2. Da es keinen neuen Teil-Lösungsschritt gibt: return false // Keine Lösung!





def dfs(graph, node):

visited_nodes = [node]

for nodes in graph[node]:

if nodes not in visited_nodes:

visited_nodes += dfs(graph, nodes)

return visited_nodes


visited = set()

stack = [start]

  

while stack:

vertex = stack.pop()

if vertex not in visited:

visited.add(vertex)

stack.extend(graph[vertex] - visited)

print(visited)