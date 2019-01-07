# Quantum-Fourier-transform
Quantum fourier transform is a discrete fourier transform of quantum states.  
<img src="https://latex.codecogs.com/gif.latex?|x\rangle&space;\xrightarrow{QFT_N}&space;\frac{1}{\sqrt{N}}&space;\sum_{y=0}^{N-1}&space;\omega^{x\bullet&space;y}&space;|y\rangle" title="|x\rangle \xrightarrow{QFT_N} \frac{1}{\sqrt{N}} \sum_{y=0}^{N-1} \omega^{x\bullet y} |y\rangle" />  
(<img src="https://latex.codecogs.com/gif.latex?\omega&space;=&space;e^{\frac{2\pi&space;i}{N}}" title="\omega = e^{\frac{2\pi i}{N}}" />)

## Example
H gate (Hadamard transformation) is quantum fourier transform for 1 qubits.  
<img src="https://latex.codecogs.com/gif.latex?|0\rangle&space;\xrightarrow{QFT_1}&space;\frac{1}{\sqrt{2}}&space;\sum_{y=0}^{1}&space;\omega^{0\bullet&space;y}&space;|y\rangle&space;=&space;\frac{|0\rangle&space;&plus;&space;|1\rangle}{\sqrt{2}}" title="|0\rangle \xrightarrow{QFT_1} \frac{1}{\sqrt{2}} \sum_{y=0}^{1} \omega^{0\bullet y} |y\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}" />  
<img src="https://latex.codecogs.com/gif.latex?|1\rangle&space;\xrightarrow{QFT_1}&space;\frac{1}{\sqrt{2}}&space;\sum_{y=0}^{1}&space;\omega^{1\bullet&space;y}&space;|y\rangle&space;=&space;\frac{|0\rangle&space;-&space;|1\rangle}{\sqrt{2}}" title="|1\rangle \xrightarrow{QFT_1} \frac{1}{\sqrt{2}} \sum_{y=0}^{1} \omega^{1\bullet y} |y\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}}" />  
(<img src="https://latex.codecogs.com/gif.latex?\omega&space;=&space;e^{{\pi&space;i}}" title="\omega = e^{{\pi i}}" />)  

## Mathematical explanation  
A decimal number in binary system is written like this.  
<img src="https://latex.codecogs.com/gif.latex?0.&space;j_1j_2j_3...j_n&space;=&space;\frac{j_1}{2}&plus;\frac{j_2}{2^2}&plus;\frac{j_3}{2^3}&plus;&space;...&space;&plus;&space;\frac{j_{n}}{2^n}" title="0. j_1j_2j_3...j_n = \frac{j_1}{2}+\frac{j_2}{2^2}+\frac{j_3}{2^3}+ ... + \frac{j_{n}}{2^n}" />  

<img src="https://latex.codecogs.com/gif.latex?e^{{2\pi&space;i}\frac{j}{2}}&space;=&space;e^{2\pi&space;i&space;0.j_1}" title="e^{{2\pi i}\frac{j}{2}} = e^{2\pi i 0.j_1}" />   
<img src="https://latex.codecogs.com/gif.latex?e^{{2\pi&space;i}\frac{j}{2^2}}&space;=&space;e^{2\pi&space;i&space;0.j_2j_1}" title="e^{{2\pi i}\frac{j}{2^2}} = e^{2\pi i 0.j_2j_1}" />  

Therefore, the total sum of QFT becomes the product of each term.  
<img src="https://latex.codecogs.com/gif.latex?|j\rangle&space;\xrightarrow{QFT_N}&space;=&space;\frac{1}{\sqrt{N}}&space;(|0\rangle&space;&plus;&space;e^{2\pi&space;i&space;0.j_N}|1\rangle)\otimes&space;(|0\rangle&space;&plus;&space;e^{2\pi&space;i&space;0.j_{N-1}j_N}|1\rangle)..&space;(|0\rangle&space;&plus;&space;e^{2\pi&space;i&space;0.j_1j_2..j_{N-1}j_N}|1\rangle)" title="|j\rangle \xrightarrow{QFT_N} = \frac{1}{\sqrt{N}} (|0\rangle + e^{2\pi i 0.j_N}|1\rangle)\otimes (|0\rangle + e^{2\pi i 0.j_{N-1}j_N}|1\rangle).. (|0\rangle + e^{2\pi i 0.j_1j_2..j_{N-1}j_N}|1\rangle)" />    
 
For instance, QFT for 2 qubits would be like this.  
<img src="https://latex.codecogs.com/gif.latex?|j\rangle&space;\xrightarrow{QFT_2}&space;=&space;\frac{1}{\sqrt{2}}&space;(|0\rangle&space;&plus;&space;e^{2\pi&space;i&space;0.j_N}|1\rangle)" title="|j\rangle \xrightarrow{QFT_2} = \frac{1}{\sqrt{2}} (|0\rangle + e^{2\pi i 0.j_N}|1\rangle)" />  
<img src="https://latex.codecogs.com/gif.latex?(x=0:&space;\frac{1}{\sqrt{2}}&space;(|0\rangle&space;&plus;&space;e^{2\pi&space;i&space;0.0}|1\rangle&space;=&space;\frac{1}{\sqrt{2}}(|0\rangle&space;&plus;&space;|1\rangle))" title="(x=0: \frac{1}{\sqrt{2}} (|0\rangle + e^{2\pi i 0.0}|1\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle))" />  
<img src="https://latex.codecogs.com/gif.latex?(x=1:&space;\frac{1}{\sqrt{2}}&space;(|0\rangle&space;&plus;&space;e^{2\pi&space;i&space;0.1}|1\rangle&space;=&space;\frac{1}{\sqrt{2}}&space;(|0\rangle&space;&plus;&space;e^{\pi&space;i}|1\rangle)&space;\frac{1}{\sqrt{2}}(|0\rangle&space;-&space;|1\rangle))" title="(x=1: \frac{1}{\sqrt{2}} (|0\rangle + e^{2\pi i 0.1}|1\rangle = \frac{1}{\sqrt{2}} (|0\rangle + e^{\pi i}|1\rangle) \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle))" /> 

## Implementation in qiskit   

In order to perform QFT, you have to multiply the following matrix.  
<img src="https://latex.codecogs.com/gif.latex?cR_k&space;=&space;\left(&space;\begin{array}{cccc}&space;1&space;&&space;0&space;&&space;0&space;&&space;0\\&space;0&space;&&space;1&space;&&space;0&space;&&space;0\\&space;0&space;&&space;0&space;&&space;1&space;&&space;0\\&space;0&space;&&space;0&space;&0&space;&&space;e^{i\frac{2\pi}{2^k}}\\&space;\end{array}&space;\right)" title="cR_k = \left( \begin{array}{cccc} 1 & 0 & 0 & 0\\ 0 & 1 & 0 & 0\\ 0 & 0 & 1 & 0\\ 0 & 0 &0 & e^{i\frac{2\pi}{2^k}}\\ \end{array} \right)" />  

If you want to perform quantum computation on your laptop, you can download qiskit(https://qiskit.org),and you have to implement a cU1(2π/2^k) gate instead of multiply a matrix itself.    

In this repository, I put the code to implement QFT for 3 qubits.  

```
num_of_qubits = 3
q = QuantumRegister(num_of_qubits)
c = ClassicalRegister(num_of_qubits)
qc = QuantumCircuit(q, c)

#Quantum Fourier Transform
qc.h(q[0])
qc.cu1(np.pi/2,q[0],q[1])
qc.cu1(np.pi/4,q[0],q[2])
qc.h(q[1])
qc.cu1(np.pi/2,q[1],q[2])
qc.h(q[2])
```  
## Result  
This is the result on the QASM simulator.  
![qft_sim](https://user-images.githubusercontent.com/45162150/50752911-31697c80-1293-11e9-8fb1-6f7bc9ab4739.png)



