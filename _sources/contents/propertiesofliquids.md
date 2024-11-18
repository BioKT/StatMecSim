---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
---
# Static properties of liquids
## The radial distribution function
Liquids are homogeneous systems, characterized by a uniform
particle density $\rho=N/V$, where $N$ is the number of particles and
$V$ is the volume. With simulations, we can interrogate their internal
structure. One of the most important quantities that can be computed
from simulations is the *radial distribution function* (in short, RDF or
$g(r)$). The RDF can be defined as the number of particles at a distance 
$r$ from another particle divided by the number at the same distance in
an ideal gas of the same density [allen2017computer]. 
Importantly,this quantity can also be accessed experimentally. 

To calculate the rdf we simply need to histogram pairwise distances and
calculate
```{math}
:label:
g(r)=\frac{V}{4\pi r^2\Delta rN^2}\sum_i^Nn_i(r,\Delta r)
```
where $\Delta r$ is the bin width and we are averaging over
reference particles the number of times we find another 
particles in a bin centered at a distance $r$, $n_i(r,\Delta r)$.
It is important to note that the RDF is dimensionless. At short
radii, the value of $g(r)$ tends to zero due to excluded volume
effects. At distances approaching the repulsive core diameter 
($\sigma$) the RDF typically peaks, reflecting the high density
coordination shell of nearest neighbours. A second peak at longer
distances is also often found. As the distribution becomes
homogeneous at longer $r$ (greater than the correlation length $\xi$),
the density reaches that of the bulk and the value of the RDF plateaus
at 1. Due to finite size effects, the calculated $g(r)$ may not
converge to 1, in which case a correction to the RDF may be necessary.


When using a rigorous definition of the RDF, we can relate it to the 
``effective pair potential'' or potential of mean force $v(r)$ as 
```{math}
:label:
g(r)=\exp{(-\beta v(r))}
```
or equivalently
```{math}
:label:
-k_BT\ln g(r)=v(r)
```

## Useful properties related to the radial distribution function 
The number of particles within a distance $r_c$ can be estimated
easily from the RDF as 
```{math}
:label
n_c = 4\pi\rho\int_0^{r_c}drr^2g(r)
```