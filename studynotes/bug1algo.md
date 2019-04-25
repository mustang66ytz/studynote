## Bug1 algorithm

### **Input:** A point robot with a tactile sensor
### **Output:** A path to the *q<sub>goal</sub>* or a conclusion no such path exists

**while** Forever **do**  
>**repeat**  
>>From *q<sub>i-1</sub><sup>L</sup>*, move toward *q<sub>goal</sub>*   

>**until** *q<sub>goal</sub>* is reached **or** an obstacle is encountered at *q<sub>i</sub><sup>H</sup>*  
>**if** Goal is reached **then**  
>>Exit   

>**end if**   
>**repeat**   
>>Follow the obstacle boundary.  

>**until** *q<sub>goal</sub>* is reached **or** *q<sub>i</sub><sup>H</sup>* is re-encountered.   
>Determine the point *q<sub>i</sub><sup>L</sup>* on the perimeter that has the shortest distance to the goal.   
>Go to *q<sub>i</sub><sup>L</sup>*   
>**if** the robot were to move toward the goal **then**   
>>Conclude *q<sub>goal</sub>* is not reacheable and exit   

>**end if**   

**end while**  

 
