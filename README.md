# SIR-model-parameter-estimation
From data on infections, determine the parameters within the SIR model in a non-linear least square sense

We first define the system of ODE from the SIR model :

$$
\begin{align}
\frac{dS}{dt} &= -\beta S I,\\
\frac{dI}{dt} &= \beta S I - \gamma I,  \\
\frac{dR}{dt} &= \gamma I, \\ 
\end{align}
$$
where the parameters sought are $\vec{\beta} = \begin{bmatrix}\beta & \gamma\end{bmatrix}^T$, $S(t)$ represents the susceptible population, $I(t)$ the infected population and $R(t)$ the recovered population.

The experimental data vector $\vec{d}(t)$ represents the number of infected people per day and will serve as the curve to be fitted.

The non-linear least square objective function is defined as
$$
F(\beta)
$$
