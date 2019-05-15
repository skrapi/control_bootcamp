<style TYPE="text/css"> code.has-jax {font: inherit; font-size: 100%; background: inherit; border: inherit;} </style> <script type="text/x-mathjax-config"> MathJax.Hub.Config({ tex2jax: { inlineMath: [['$','$'], ['\\(','\\)']], skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'] // removed 'code' entry } }); MathJax.Hub.Queue(function() { var all = MathJax.Hub.getAllJax(), i; for(i = 0; i < all.length; i += 1) { all[i].SourceElement().parentNode.className += ' has-jax'; } }); </script> <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-AMS_HTML-full"></script>

# Stability and Eigenvalues

## Stability

$x(t) = Te^{Dt}T^{-1}x(0)$ 

$
e^{Dt} = \begin{bmatrix}
e^{\lambda_1 t} &&& \\
& e^{\lambda_2 t} & \text{\huge0} &\\
& \text{\huge0}& \ddots && \\
&&&& e^{\lambda_n t} \\
\end{bmatrix}
$

* What happens when $t \rightarrow \infty$
  
The system is stable is all eigenvalues have negative real parts:

$\lambda_i = a_i+jb_i, a_i<0 for \ all \ i$

## Discrete Stability

$x_{k+1} = \tilde{A}x_k, \ x_k=x(k\Delta t)$

$\tilde{A} = e^{A\Delta t}$

$x_1 = \tilde{A}x_0, \lambda$

$x_2 = \tilde{A}^2x_0, \lambda^2$

$x_N = \tilde{A}^Nx_0, \lambda^N$

$\lambda=Re^{i\theta}$

$\lambda^N=R^Ne^{iN\theta}$

$\tilde{A} = \tilde{T}\tilde{D}\tilde{T}^{-1}$

This system is stable if all eigenvalues $\tilde{\lambda_i}$ have a radius of less than 1
