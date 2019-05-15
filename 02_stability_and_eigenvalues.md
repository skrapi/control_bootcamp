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
  
The system is stable is all eigenvalues have negative real parts