
# This is a test of markdown editing in Jupyter.

I'm mainly interested in testing the limits of the $\LaTeX$ formatting. It appears to support most things, including inline equations: $\hbar = 1.0545718\times 10^{-34}\: kg\cdot m^2/s$, standalone equations:

$$
    x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a}
$$

multi-line equation blocks (using "aligned"):

$$
\begin{aligned}
    \nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} \\
    \nabla \cdot \mathbf{B} &= 0 \\
    \nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} \\
    \nabla \times \mathbf{B} &= \mu_0\left(\mathbf{J}+\varepsilon_0\frac{\partial \mathbf{E}}{\partial t}\right)
\end{aligned}
$$

several "amssymb" characters:

$\forall\; a,\, b \in \mathbb{R}\; \text{st.}\; a \le b\; \exists\; c \in \mathbb{R}\; \text{st.}\; a \le c \le b$



$$
    \sum_{n=0}^{\infty}\frac{1}{2^n} = 2
$$

but not equation numbering. Or, at least, it doesn't support the "label" and "ref" method of equation numbering and referencing, and I haven't figured out any other syntax that does work.
