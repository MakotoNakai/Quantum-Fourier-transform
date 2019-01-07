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
In order to perform QFT,
If you want to perform quantum computation on your laptop, you can download qiskit(https://qiskit.org). In order to perform QFT on qiskit, you have to implement a cU1(2π/2^k) gate

