# Linear Systems Notes
<style TYPE="text/css"> code.has-jax {font: inherit; font-size: 100%; background: inherit; border: inherit;} </style> <script type="text/x-mathjax-config"> MathJax.Hub.Config({ tex2jax: { inlineMath: [['$','$'], ['\\(','\\)']], skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'] // removed 'code' entry } }); MathJax.Hub.Queue(function() { var all = MathJax.Hub.getAllJax(), i; for(i = 0; i < all.length; i += 1) { all[i].SourceElement().parentNode.className += ' has-jax'; } }); </script> <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-AMS_HTML-full"></script>


## System model
Underline means vector, double underline means matrix

System model:
$\dot{\underline{x}} = \underline{\underline{A}}\ \underline{x}, \  x \ \epsilon \ \R^{n}$

Ideal Solution: $x(t) = e^{At}x(0)$

Taylor series approx of $e^{At}$:

$e^{At} = I + At + \frac{A^2t^2}{2!} + \frac{A^3t^3}{3!} + \dots$

We need a coordinate transfer from the above to an eigenvalue and eigenvector respresentation

## Eigenvalues & Eigenvectors

Eigenvalue will result in the same scaling of an eigenvector as the matrix applied to it

$\underline{\underline{A}}\ \underline{\xi_i} = \lambda_i\underline{\xi_i}$

$\xi$ is an eigenvector if the above equation holds, and then a matrix of these vectors would be:

$T = \begin{bmatrix}
\xi_1 & \xi_2 & \dots & \xi_n \\
\end{bmatrix}$

And $\lambda_i$ is the eigenvalue, and a matrix of them woud be:

$D= \begin{bmatrix}
\lambda_1 &&& \\
& \lambda_2 & \text{\huge0} &\\
& \text{\huge0}& \ddots & \\
&&& \lambda_n \\
\end{bmatrix}$

$ AT =TD $

$ D = T^{-1} A T $

$ \dot{x} = T \dot{z} = Ax $

$ T\dot{z} =  ATz$

$ \dot{z} = T^{-1} A Tz $ 

$ \dot{z} = Dz$ 

Diagonal dynamics mean the states are uncoupled from each other.

``` matlab
[T, D] = eig(A);
```
$ 
z(t) = e^{Dt}z(0) = \begin{bmatrix}
e^{\lambda_1 t} &&& \\
& e^{\lambda_2 t} & \text{\huge0} &\\
& \text{\huge0}& \ddots && \\
&&&& e^{\lambda_n t} \\
\end{bmatrix}\
$



