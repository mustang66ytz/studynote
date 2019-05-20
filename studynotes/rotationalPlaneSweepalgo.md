## Rotational Plane Sweep algorithm

### **Input:** A set of vertices {v<sub>i</sub>} (whose edges do not intersect) and a vertex v
### **Output:** A subset of vertices from {v<sub>i</sub>} that are within the line of sight of v

For each vertex v<sub>i</sub>, calculate alpha<sub>i</sub>, the angle from the horizontal axis to the line segment vv<sub>i</sub>  
Create the vertex list *E*, containing the alpha<sub>i</sub>'s stored in increasing order  
Create the active list *S*, containing the sorted list of edges that intersect the horizontal half-line emananting from v  
**for all** alpha<sub>i</sub> **do**  
>**if** v<sub>i</sub> is visible to v **then**  
>>Add the edge (v, v<sub>i</sub>) to the visibility graph 
>>From *q<sub>i-1</sub><sup>L</sup>*, move toward *q<sub>goal</sub>*   
>**end if**   
>**if** v<sub>i</sub> is the beginning of an edge *e*, not in **S** **then**  
>>Insert the *e* into **S**  
>**end if**   
>**if** v<sub>i</sub> is the end of an edge in **S** **then**  
>>Delete the edge from **S**  
>**end if**   

**end for**  
