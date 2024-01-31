---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
---
# Classical mechanics
## Newton's equations 
We will start this course with a reminder of Newton's equations of motion,
formulated by English physicist and mathematitian Sir Isaac Newton in 
the *Philosophiae Naturalis Principia Mathematica* in 1687. The laws
establish the following:
* In the absence of external forces, a body will either be at rest or
continue its motion following a straight line with a constant velocity, 
$\mathbf{v}_i$.
* An eternal force $\mathbf{f}_i$ on a body produces an acceleration equal
to the force divided by the mass of the body, or
\begin{equation}
m_i\ddot{\mathbf{r}}_i=\mathbf{f}_i(\mathbf{r}_i)
\end{equation} 
* If a body A exerts a force on another body, B, then body B exerts a force
in body A such that
\begin{equation}
\bf{f}_{AB}=-\bf{f}_{BA}
\end{equation}
Here we are already introducing a certain amount of notation. For a particle $i$
its Cartesian coordinates are expressed using vector $\mathbf{r}_i$. Hence
for a system with $N$ particles we will denote the position vectors collectively
as $\mathbf{r}^N$. Also, we are using the force vector $\mathbf{f}_i$, corresponding
to the force acting on particle $i$. This force can be obtained as a partial 
derivative of a potential $V$, specifying the interactions in the $N$ particle
system
\begin{equation}
\mathbf{f}_i(\mathbf{r}^N)=-\frac{\partial V(\mathbf{r}^N)}{\partial \mathbf{r}_i}
\label{eq:force}
\end{equation}
For most of this course, the potential energy that we will be considering will be
due to molecular interactions that we will consider to be pair-wise additive
and dependent on the distance between particles. Hence,
\begin{equation}
V(\mathbf{r}^N)=\sum_{i=1}^N\sum_{j=i+1}^Nv(r_{ij})
\end{equation}
where we are avoiding double-counting of interactions in the sums. We can
substitute in Equation \ref{eq:force} and see that the force acting on particle $i$
is in fact a sum over pairwise forces
\begin{equation}
\mathbf{f}_i=-\frac{\partial V(\mathbf{r}^N)}{\partial \mathbf{r}_i} = 
-\sum_{i=1}^N\sum_{j=i+1}^N\frac{\partial v(r_{ij})}{\partial \mathbf{r}_i}
=\sum_{i\neq j}^N \mathbf{f}_{ij} 
\end{equation}
## Energy conservation
