## Bug2 algorithm

### **Input:** A point robot with a tactile sensor
### **Output:** A path to the *q<sub>goal</sub>* or a conclusion no such path exists

**while** True **do**  
>**repeat**  
>>From *q<sub>i-1</sub><sup>L</sup>*, move toward *q<sub>goal</sub>* along m-line      

>**until** *q<sub>goal</sub>* is reached **or** an obstacle is encountered at hit point *q<sub>i</sub><sup>H</sup>*  
>Turn left or right  
>**repeat**  
>>Follow boundary  

>**until**  
>>*q<sub>goal</sub>* is reached **or**   
>>*q<sub>i</sub><sup>H</sup>* is re-encountered **or**  
>>m-line is re-encountered at a point m such that   
>>>m!=*q<sub>i</sub><sup>H</sup>* robot did not reach the hit point  
>>>d\(m, q<sub>goal</sub>\) < d\(m, q<sub>i</sub><sup>H</sup>\) is closer, and  
>>>If robot moves toward goal, it would not hit the obstacle   

>Let *q<sub>i+1</sub><sup>L</sup>* = *m*   
>Increment *i*

**end while**  
