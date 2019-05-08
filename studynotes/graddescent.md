## Gradient Descent algorithm

### **Input:** A means to compute the gradient *deltaU(q)* at a point *q*
### **Output:** A sequence of points *q(0), q(1), q(2), ..., q(i)*

*q(0) = q<sub>start</sub>*  
*i = 0*  
**while** deltaU(q) != 0 **do**  
>*q(i+1) = q(i) + alpha(i)deltaU(q(i)) *  
>*i = i+1*  

**end while**  

