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
* In the absence of external forces, a particle $i$ will either be at rest or
continue its motion following a straight line with a constant velocity, 
$\mathbf{v}_i$.
* An eternal force $\mathbf{f}_i$ on a body produces an acceleration equal
to the force divided by the mass of the body, or
```{math}
:label:
m_i\ddot{\mathbf{r}}_i=\mathbf{f}_i(\mathbf{r}_i)
```
* If a body A exerts a force on another body, B, then body B exerts a force
in body A such that
```{math}
:label:
\bf{f}_{AB}=-\bf{f}_{BA}
```
Here we are already introducing a certain amount of notation. For a particle $i$
its Cartesian coordinates are expressed using vector $\mathbf{r}_i$. Hence
for a system with $N$ particles we will denote the position vectors collectively
as $\mathbf{r}^N$. Also, we are using the force vector $\mathbf{f}_i$, corresponding
to the force acting on particle $i$. This force can be obtained as a partial 
derivative of a potential $V$, specifying the interactions in the $N$ particle
system
```{math}
:label: eq-force
\mathbf{f}_i(\mathbf{r}^N)=-\frac{\partial V(\mathbf{r}^N)}{\partial \mathbf{r}_i}
```
For most of this course, the potential energy that we will be considering will be
due to molecular interactions that we will consider to be pair-wise additive
and dependent on the distance between particles. Hence,
```{math}
:label:
V(\mathbf{r}^N)=\sum_{i=1}^N\sum_{j=i+1}^Nv(r_{ij})
```
where we are avoiding double-counting of interactions in the sums. We can
substitute in Equation {eq}`eq-force` and see that the force acting on particle $i$
is in fact a sum over pairwise forces
```{math}
:label:
\mathbf{f}_i=-\frac{\partial V(\mathbf{r}^N)}{\partial \mathbf{r}_i} = 
-\sum_{i=1}^N\sum_{j=i+1}^N\frac{\partial v(r_{ij})}{\partial \mathbf{r}_i}
=\sum_{i\neq j}^N \mathbf{f}_{ij} 
```

## Energy conservation
One of the most fundamental properties of the mechanical systems that we will
consider in this course is energy conservation. In general, we can write
the hamiltonian of the system ($\mathcal{H}$) as the sum of the kinetic energy ($K$) and the potential
energy ($V$), 
```{math}
:label:
H = K + V
```
where 
```{math}
:label:
K=\sum_i^N\frac{1}{2}m_i\dot{\mathbf{r}}_i^2=\sum_i^N\frac{\mathbf{p}_i^2}{2m_i}
```
Because $H$ is a constant of motion, we have
```{math}
:label:
\frac{d\mathcal{H}}{dt}=0
```
which can be further expanded as
```{math}
:label:
\frac{d\mathcal{H}}{dt}=\frac{d}{dt}\bigg[\sum_i^N\frac{\mathbf{p}_i^2}{2m_i} + V\bigg]
```
