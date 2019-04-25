## Bug1 algorithm

### **Input:** A point robot with a tactile sensor
### **Output:** A path to the *q<sub>goal</sub>* or a conclusion no such path exists

**while** Forever **do**  
  **repeat**  
    From *q<sub>i-1</sub><sup>L</sup>*, move toward *q<sub>goal</sub>*   
  **until** *q<sub>goal</sub>* is reached **or** an obstacle is encountered at *q<sub>i</sub><sup>H</sup>*\s\s
  **if** Goal is reached **then**\s\s
    Exit\s\s
  **end if**\s\s
  **repeat**\s\s
    Follow the obstacle boundary.\s\s
  **until** *q<sub>goal</sub>* is reached **or** *q<sub>i</sub><sup>H</sup>* is re-encountered.\s\s
  Determine the point *q<sub>i</sub><sup>L</sup>* on the perimeter that has the shortest distance to the goal.\s\s
  Go to *q<sub>i</sub><sup>L</sup>*\s\s
  **if** the robot were to move toward the goal **then**\s\s
    Conclude *q<sub>goal</sub>* is not reacheable and exit\s\s
  **end if**\s\s
**end while** 

