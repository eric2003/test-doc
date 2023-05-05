Navier–Stokes equations
==================================

In physics, the Navier–Stokes equations (/nævˈjeɪ stoʊks/ nav-YAY STOHKS) are partial differential equations which describe the motion of viscous fluid substances, named after French engineer and physicist Claude-Louis Navier and Anglo-Irish physicist and mathematician George Gabriel Stokes. They were developed over several decades of progressively building the theories, from 1822 (Navier) to 1842-1850 (Stokes).

Control Mass(CM) &Control Volume (CV)
--------------------------------------

Conservation laws can be derived by considering a given quantity of matter or 
control mass (CM) and its extensive properties, such as mass, momentum and 
energy. This approach is used to study the dynamics of solid bodies, where the 
CM (sometimes called the system) is easily identified. In fluid flows, however, 
it is difficult to follow a parcel of matter. It is more convenient to deal with 
the flow within a certain spatial region we call a control volume (CV), rather 
than in a parcel of matter which quickly passes through the region of interest. 
This method of analysis is called the control volume approach.  

Examples are density :math:`\rho` (mass per unit volume) 
and velocity :math:`v \mathbf{v} \boldsymbol{v}` (momentum per unit mass).

If :math:`\phi` is any conserved intensive property (for mass conservation, :math:`\phi=1`;  for 
momentum conservation, :math:`\phi=\boldsymbol{v}`;  for conservation of a scalar, :math:`\phi` represents the 
conserved property per unit mass), then the corresponding extensive property 
:math:`\Phi` can be expressed as:

.. math::    
  \Phi =\int_{\Omega _{CM} } \rho \phi d\Omega
  
where :math:`\Omega_{CM}` stands for volume occupied by the CM.  
  
Reynolds' transport theorem
------------------------------

.. math::

  \cfrac{\mathrm{d}}{\mathrm{d}t}\int_{\Omega(t)} \mathbf{f}~\text{dV} = 
  \int_{\Omega(t)} \frac{\partial \mathbf{f}}{\partial t}~\text{dV} + \int_{\partial \Omega(t)} (\mathbf{v}_{\mathrm{b}}\cdot\mathbf{n})\mathbf{f}~\text{dA}~ ~
  
.. math::  
  \frac{\mathrm{d}}{\mathrm{d} t} \int_{\Omega_{\mathrm{CM}}} \rho \phi \mathrm{d} \Omega=
  \frac{\mathrm{d}}{\mathrm{d} t} \int_{\Omega_{\mathrm{CV}}} \rho \phi \mathrm{d} \Omega+
  \int_{S_{\mathrm{CV}}} \rho \phi\left(\boldsymbol{v}-\boldsymbol{v}_{\mathrm{b}}\right) \cdot n \mathrm{~d} S
  
where :math:`\Omega_{\mathrm{CV}}` is the CV volume, :math:`S_{\mathrm{CV}}` is the surface enclosing CV, :math:`\boldsymbol{n}` is the unit 
vector orthogonal to :math:`S_{\mathrm{CV}}` and directed outwards, :math:`\boldsymbol{v}` is the fluid velocity and :math:`\boldsymbol{v}_{\mathrm{b}}` 
is the velocity with which the CV surface is moving. For a fixed CV, which 
we shall be considering most of the time, :math:`\boldsymbol{v}_{\mathrm{b}}=0` and the first derivative 
on the right hand side becomes a local (partial) derivative. This equation 
states that the rate of change of the amount of the property in the control 
mass, :math:`\Phi`, is the rate of change of the property within the control volume plus 
the net flux of it through the CV boundary due to fluid motion relative to 
CV boundary. The last term is usually called the convective (or sometimes, 
advective) flux of :math:`\phi` through the CV boundary. If the CV moves so that its 
boundary coincides with the boundary of a control mass, then :math:`\boldsymbol{v}=\boldsymbol{v}_{\mathrm{b}}`  and 
this term will be zero as required. 
A detailed derivation of this equation is given in in many textbooks on 
fluid dynamics (e.g. in Bird et al., 1962; Fox and McDonald, 1982) and will not 
be repeated here. The mass, momentum and scalar conservation equations 
will be presented in the next three sections. For convenience, a fixed CV will 
be considered; :math:`\Omega` represents the CV volume and S its surface.  


Conservation Equations
------------------------------

Conservation Laws
`````````````````````````````
One group of the fundamental equations of continuum mechanics arises from the conservation
laws. These equations must always be satisfied by physical systems. Four conservation laws
relevant to thermomechanical systems are considered here:

#. Conservation of mass
#. Conservation of linear momentum, often called conservation of momentum
#. Conservation of energy
#. Conservation of angular momentum.

The conservation laws are also known as balance laws, for example, the conservation of
energy is often called the balance of energy.

Material Time Derivative of an Integral and Reynolds’ Transport Theorem
```````````````````````````````````````````````````````````````````````````````````````
The material time derivative of an integral is the rate of change of an integral on a material
domain. A material domain moves with the material, so that the material points on the
boundary remain on the boundary and no mass flux occurs across the boundaries. A material
domain is analogous to a Lagrangian mesh; a Lagrangian element or group of Lagrangian elements is a nice example of a material domain. The various forms for material time derivatives
of integrals are called Reynolds’ transport theorem.

The material time derivative of an integral is defined by

.. math::
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }^{}f(\mathbf{x},t)\mathrm{d}\Omega 
  =\lim_{\Delta  t \to 0}\cfrac{1}{\Delta  t }\left ( \int\limits_{\Omega_{\tau+\Delta t} }f(\mathbf{x},{\tau+\Delta t})\mathrm{d}\Omega-\int\limits_{\Omega_{\tau} }f(\mathbf{x},\tau )\mathrm{d}\Omega \right )
  
where :math:`\Omega_{\tau}`
t is the spatial domain at time :math:`{\tau}` and :math:`\Omega_{\tau+\Delta t}` is the spatial domain occupied by the same
material points at time :math:`{\tau+\Delta t}`. The notation on the left-hand side is a little confusing because it
appears to refer to a single spatial domain. However, in this notation, which is standard, the material derivative on the integral implies that the domain Ω is a material domain. We now
transform both integrals on the RHS to the reference domain:

.. math::
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }f(\mathbf{x},t)\mathrm{d}\Omega 
  =\lim_{\Delta  t \to 0}\cfrac{1}{\Delta  t }\left ( \int\limits_{\Omega_{0} }f(\mathbf{X},{\tau+\Delta t})J(\mathbf{X},{\tau+\Delta t})\mathrm{d}\Omega_{0}-\int\limits_{\Omega_{0} }f(\mathbf{X},\tau )J(\mathbf{X},\tau )\mathrm{d}\Omega_{0} \right )
  
With this change in the domain of integration, :math:`{f}` becomes a function of the material coordinates, that is, :math:`f(\mathbf{\Phi}(\mathbf{X},t),t)\equiv f\circ \mathbf{\Phi}`.

Since the domain of integration is now independent of time, we can pull the limit operation
inside the integral and take the limit, which yields  

.. math::
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }f(\mathbf{x},t)\mathrm{d}\Omega 
  =\int\limits_{\Omega_{0} }\frac{\partial }{\partial t}[f(\mathbf{X},t)J(\mathbf{X},t)] \mathrm{d}\Omega_{0}
  
The partial derivative with respect to time in the integrand is a material time derivative since
the independent space variables are the material coordinates. We next use the product rule for
derivatives on the previous:

.. math::
  \begin{align}
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }f(\mathbf{x},t)\mathrm{d}\Omega 
  =\int\limits_{\Omega_{0} }\frac{\partial }{\partial t}[f(\mathbf{X},t)J(\mathbf{X},t)] \mathrm{d}\Omega_{0}\\
  =\int\limits_{\Omega_{0} }(\frac{\partial f(\mathbf{X},t)}{\partial t}J(\mathbf{X},t)+f(\mathbf{X},t)\frac{\partial J(\mathbf{X},t)}{\partial t}) \mathrm{d}\Omega_{0}\\
  \end{align}

-

.. math::  
  \begin{align}
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }f(\mathbf{x},t)\mathrm{d}\Omega 
  =\int\limits_{\Omega_{0} }\frac{\partial }{\partial t}[f(\mathbf{X},t)J(\mathbf{X},t)] \mathrm{d}\Omega_{0}\\
  =\int\limits_{\Omega_{0} }(\frac{\partial f(\mathbf{X},t)}{\partial t}J(\mathbf{X},t)+f(\mathbf{X},t)\frac{\partial J(\mathbf{X},t)}{\partial t}) \mathrm{d}\Omega_{0}\\
  =\int\limits_{\Omega_{0} }(\frac{\partial f(\mathbf{X},t)}{\partial t}J(\mathbf{X},t)+f(\mathbf{X},t)J(\mathbf{X},t)\frac{\partial v_{k}}{\partial x_{k}}) \mathrm{d}\Omega_{0}\\
  \end{align}
  
We can now transform the RHS integral to the current domain and change the
independent variables to an Eulerian description, which gives

.. math:: 
  \begin{align}
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }f(\mathbf{x},t)\mathrm{d}\Omega 
  =\int\limits_{\Omega }(\frac{D f(\mathbf{x},t)}{D t}+f(\mathbf{x},t)\frac{\partial v_{k}}{\partial x_{k}}) \mathrm{d}\Omega\\
  \end{align}
  
where we have used :math:`{D f(\mathbf{x},t)}/{D t}\equiv \partial f(\mathbf{X},t)/\partial t`. This is one form of
Reynolds’ transport theorem. 
 
.. math:: 
  \cfrac{\mathrm{D}  f}{\mathrm{D} t}=\cfrac{\partial f}{\partial t}+v_{i} \cfrac{\partial f}{\partial x_{i}}=\cfrac{\partial f}{\partial t}+\mathbf{v} \cdot \nabla f=\cfrac{\partial f}{\partial t}+\mathbf{v} \cdot \operatorname{grad} f \\
  
-  
  
.. math::   
  \begin{array}{l}
  \cfrac{\mathrm{D} f(\mathbf{x},t)}{\mathrm{D} t}&=\cfrac{\partial f(\mathbf{x},t)}{\partial t}+v_{i}(\mathbf{x},t) \cfrac{\partial f(\mathbf{x},t)}{\partial x_{i}}\\
  &=\cfrac{\partial f(\mathbf{x},t)}{\partial t}+\mathbf{v}(\mathbf{x},t) \cdot \nabla f(\mathbf{x},t)\\
  &=\cfrac{\partial f(\mathbf{x},t)}{\partial t}+\mathbf{v}(\mathbf{x},t) \cdot \operatorname{grad} f(\mathbf{x},t) \\
  \end{array}  

-  
  
.. math:: 
  \begin{align}
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }f(\mathbf{x},t)\mathrm{d}\Omega 
  &=\int\limits_{\Omega }(\frac{D f(\mathbf{x},t)}{D t}+f(\mathbf{x},t)\frac{\partial v_{k}}{\partial x_{k}}) \mathrm{d}\Omega\\
  &=\int\limits_{\Omega }(\cfrac{\partial f(\mathbf{x},t)}{\partial t}+v_{k}(\mathbf{x},t) \cfrac{\partial f(\mathbf{x},t)}{\partial x_{k}}+f(\mathbf{x},t)\frac{\partial v_{k}}{\partial x_{k}}) \mathrm{d}\Omega\\
  &=\int\limits_{\Omega }(\cfrac{\partial f(\mathbf{x},t)}{\partial t}+\cfrac{\partial (v_{k}(\mathbf{x},t)f(\mathbf{x},t))}{\partial x_{k}}) \mathrm{d}\Omega\\
  \end{align}
  
which can be written in tensor form as

.. math:: 
  \begin{align}
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }f(\mathbf{x},t)\mathrm{d}\Omega 
  &=\int\limits_{\Omega }(\cfrac{\partial f(\mathbf{x},t)}{\partial t}+\mathrm{div}\ (\mathbf{v}(\mathbf{x},t)\cdot f(\mathbf{x},t)) \mathrm{d}\Omega\\
  &=\int\limits_{\Omega }(\cfrac{\partial f(\mathbf{x},t)}{\partial t}+\nabla\cdot(\mathbf{v}(\mathbf{x},t)\cdot f(\mathbf{x},t)) \mathrm{d}\Omega\\
  \end{align}

-
  
.. math::
  \begin{align}
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }f(\mathbf{x},t)\mathrm{d}\Omega 
  &=\int\limits_{\Omega }(\cfrac{\partial f(\mathbf{x},t)}{\partial t}) \mathrm{d}\Omega
  +\int\limits_{\Omega }(\nabla\cdot(\mathbf{v}(\mathbf{x},t)\cdot f(\mathbf{x},t)) \mathrm{d}\Omega\\
  &=\int\limits_{\Omega }(\cfrac{\partial f(\mathbf{x},t)}{\partial t}) \mathrm{d}\Omega
  +\int\limits_{\Gamma }f(\mathbf{x},t)(\mathbf{v}(\mathbf{x},t)\cdot \mathbf{n}(\mathbf{x},t)) \mathrm{d}\Gamma \\
  &=\int\limits_{\Omega }(\cfrac{\partial f(\mathbf{x},t)}{\partial t}) \mathrm{d}\Omega
  +\int\limits_{\Gamma }f(\mathbf{x},t)({v}_{k}(\mathbf{x},t){n}_{k}(\mathbf{x},t)) \mathrm{d}\Gamma \\
  \end{align}
  
Mass Conservation
-------------------

The mass :math:`m(\Omega)` of a material domain:math:`\Omega` is given by

.. math::
  m(\Omega)=\int\limits_{\Omega }\rho (\mathbf{x},t) \mathrm{d}\Omega  
  
where :math:`\rho (\mathbf{x},t)` is the density. Mass conservation requires that the mass of any material domain
be constant, since no material flows through the boundaries of a material domain and we are
not considering mass to energy conversion. Therefore, according to the principle of mass
conservation, the material time derivative of :math:`m(\Omega)` vanishes, that is,  

.. math::
  \cfrac{\mathrm{D} m(\Omega)}{\mathrm{D} t} =\cfrac{\mathrm{D}}{\mathrm{D} t}\int\limits_{\Omega }\rho (\mathbf{x},t) \mathrm{d}\Omega=0
  
Applying Reynolds’ theorem

.. math::
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }\rho(\mathbf{x},t)\mathrm{d}\Omega 
  =\int\limits_{\Omega }(\frac{D \rho(\mathbf{x},t)}{D t}+\rho(\mathbf{x},t)\frac{\partial v_{k}}{\partial x_{k}}) \mathrm{d}\Omega=0\\

-

.. math::
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }\rho(\mathbf{x},t)\mathrm{d}\Omega 
  =\int\limits_{\Omega }(\frac{D \rho(\mathbf{x},t)}{D t}+\rho(\mathbf{x},t)\nabla \mathbf{v}) \mathrm{d}\Omega=0\\  
  
-

.. math::  
  \frac{D \rho(\mathbf{x},t)}{D t}+\rho(\mathbf{x},t)\frac{\partial v_{k}}{\partial x_{k}}=0
  
- 
 
.. math::  
  \frac{D \rho(\mathbf{x},t)}{D t}+\rho(\mathbf{x},t)\nabla \cdot\mathbf{v}=0  
  
Conservation of Linear Momentum
--------------------------------------

The equation emanating from the principle of linear momentum conservation is a key equation
in nonlinear finite element procedures. Linear momentum conservation is equivalent to
Newton’s second law of motion, which relates the forces acting on a body to its acceleration.
The principle is often called the momentum conservation principle, or the balance of
momentum principle.

We will here state the principle in integral form and then derive an equivalent partial
differential equation. We consider an arbitrary domain :math:`\Omega` with boundary :math:`\Gamma` subjected to body
forces :math:`\rho \mathbf{b}` and to surface tractions :math:`\mathbf{t}`, where :math:`\mathbf{b}` is a force per unit mass and :math:`\mathbf{t}` is a force per unit
area. The total force is given by

.. math::  
  \mathbf {f}(t)=\int\limits_{\Omega }\rho(\mathbf{x},t)\mathbf{b}(\mathbf{x},t)\mathrm{d}\Omega 
  +\int\limits_{\Gamma  }\mathbf{t}(\mathbf{x},t)\mathrm{d}\Gamma 
  
The linear momentum is given by

.. math::
  \mathbf {p}(t)=\int\limits_{\Omega }\rho(\mathbf{x},t)\mathbf{v}(\mathbf{x},t)\mathrm{d}\Omega 
  
where :math:`\rho\mathbf{v}` is the linear momentum per unit volume.

Newton’s second law of motion for a continuum, the momentum conservation principle,
states that the material time derivative of the linear momentum equals the net force.

.. math::
  \cfrac{\mathrm{D} \mathbf{p}(t)}{\mathrm{D} t} = \mathbf {f}(t)
  
-

.. math::
  \cfrac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }\rho(\mathbf{x},t)\mathbf{v}(\mathbf{x},t)\mathrm{d}\Omega 
  =\int\limits_{\Omega }\rho(\mathbf{x},t)\mathbf{b}(\mathbf{x},t)\mathrm{d}\Omega 
  +\int\limits_{\Gamma  }\mathbf{t}(\mathbf{x},t)\mathrm{d}\Gamma 

-

.. math:: 
  \begin{align}
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }f(\mathbf{x},t)\mathrm{d}\Omega 
  =\int\limits_{\Omega }(\frac{D f(\mathbf{x},t)}{D t}+f(\mathbf{x},t)\frac{\partial v_{k}}{\partial x_{k}}) \mathrm{d}\Omega\\
  \end{align}
  
-

.. math:: 
  \begin{align}
  \frac{\mathrm{D} }{\mathrm{D} t}\int\limits_{\Omega }\rho(\mathbf{x},t)\mathbf{v}(\mathbf{x},t)\mathrm{d}\Omega 
  =\int\limits_{\Omega }\left (\frac{D (\rho(\mathbf{x},t)\mathbf{v}(\mathbf{x},t))}{D t}+(\rho(\mathbf{x},t)\mathbf{v}(\mathbf{x},t))\nabla \cdot \mathbf{v}(\mathbf{x},t) \right)\mathrm{d}\Omega\\
  \end{align}  
  
ALE Form of Conservation Equations
-----------------------------------------

To serve as an introduction to the discussion of ALE finite element and finite volume models,
we establish in this section the differential and integral forms of the conservation equations for
mass, momentum, and energy.

Differential forms
`````````````````````````
The ALE differential form of the conservation equations for mass, momentum, and energy are
readily obtained from the corresponding well-known Eulerian forms

.. math::
  \begin{align}
  &Mass:     &\frac{\mathrm{d} \rho}{\mathrm{d} t}  &= \left.\frac{\partial \rho}{\partial t}\right|_{\mathbf{x}}+\mathbf{v} \cdot \nabla \rho  = -\rho {\nabla} \cdot \mathbf{v} \\
  &Momentum:  &\rho \frac{\mathrm{d} \mathbf{v}}{\mathrm{d} t}  &= \rho\left(\left.\frac{\partial \mathbf{v}}{\partial t}\right|_{\mathbf{x}}+(\mathbf{v} \cdot {\nabla}) \mathbf{v}\right)  = {\nabla} \cdot \boldsymbol{\sigma}+\rho \mathbf{b} \\
  &Energy:   &\rho \frac{\mathrm{d} E}{\mathrm{~d} t}  &= \rho\left(\left.\frac{\partial E}{\partial t}\right|_{\mathbf{x}}+\mathbf{v} \cdot \nabla E\right)  = \nabla \cdot(\boldsymbol{\sigma} \cdot \mathbf{v})+\mathbf{v} \cdot \rho \mathbf{b} 
  \end{align}
  
where :math:`\rho` is the mass density, :math:`\mathbf{v}` is the material velocity vector, :math:`\boldsymbol{\sigma}` denotes the Cauchy stress
tensor, :math:`\mathbf{b}` is the specific body force vector, and E is the specific total energy. Only mechanical
energies are considered in the above form of the energy equation. Note that the stress term in
the same equation can be rewritten in the form  

.. math::
  {\nabla} \cdot(\boldsymbol{\sigma} \cdot \mathbf{v})=\frac{\partial\left(\sigma_{i j} v_{j}\right)}{\partial x_{i}}=\frac{\partial \sigma_{i j}}{\partial x_{i}} v_{j}+\sigma_{i j} \frac{\partial v_{j}}{\partial x_{i}}=({\nabla} \cdot \boldsymbol{\sigma}) \cdot \mathbf{v}+\boldsymbol{\sigma}: {\nabla} \mathbf{v}
  
where :math:`\nabla \mathbf{v}` is the spatial velocity gradient.

.. math::
  \nabla \rho=\begin{bmatrix}
  \cfrac{\partial \rho}{\partial x}\\
  \cfrac{\partial \rho}{\partial y}\\
  \cfrac{\partial \rho}{\partial x}
  \end{bmatrix}
  =\begin{bmatrix}
  \cfrac{\partial \rho}{\partial x_{1}}\\
  \cfrac{\partial \rho}{\partial x_{2}}\\
  \cfrac{\partial \rho}{\partial x_{3}}
  \end{bmatrix}
  =\cfrac{\partial \rho}{\partial x}\mathbf{i}
  +\cfrac{\partial \rho}{\partial y}\mathbf{j}
  +\cfrac{\partial \rho}{\partial z}\mathbf{k}
  =\cfrac{\partial \rho}{\partial x_{1}}\mathbf{e_{1}}
  +\cfrac{\partial \rho}{\partial x_{2}}\mathbf{e_{2}}
  +\cfrac{\partial \rho}{\partial x_{3}}\mathbf{e_{3}}

All one has to do to obtain the ALE form of the above conservation equations is to replace
in the various convective terms, the material velocity :math:`\mathbf{v}` with the convective velocity :math:`\mathbf{c}=\mathbf{v}-\hat {\mathbf{v}}`.
The result is

.. math::
  \begin{align}
  &Mass:     &\frac{\mathrm{d} \rho}{\mathrm{d} t}  &= \left.\frac{\partial \rho}{\partial t}\right|_{\boldsymbol\chi}+\mathbf{c} \cdot \nabla \rho  = -\rho {\nabla} \cdot \mathbf{v} \\
  &Momentum:  &\rho \frac{\mathrm{d} \mathbf{v}}{\mathrm{d} t}  &= \rho\left(\left.\frac{\partial \mathbf{v}}{\partial t}\right|_{\boldsymbol\chi}+(\mathbf{c} \cdot {\nabla}) \mathbf{v}\right)  = {\nabla} \cdot \boldsymbol{\sigma}+\rho \mathbf{b} \\
  &Energy:   &\rho \frac{\mathrm{d} E}{\mathrm{~d} t}  &= \rho\left(\left.\frac{\partial E}{\partial t}\right|_{\boldsymbol\chi}+\mathbf{c} \cdot \nabla E\right)  = \nabla \cdot(\boldsymbol{\sigma} \cdot \mathbf{v})+\mathbf{v} \cdot \rho \mathbf{b} 
  \end{align}

Integral forms  
`````````````````````````

Navier–Stokes equations
-----------------------------------------

.. math::
  \cfrac{\partial \mathbf{Q}}{\partial t} 
  +\cfrac{\partial \mathbf{E}}{\partial x}
  +\cfrac{\partial \mathbf{F}}{\partial y}
  +\cfrac{\partial \mathbf{G}}{\partial z}
  =\cfrac{\partial \mathbf{E}_{v}}{\partial x}
  +\cfrac{\partial \mathbf{F}_{v}}{\partial y}
  +\cfrac{\partial \mathbf{G}_{v}}{\partial z}
  
-

.. math::
  \begin{align}
  \mathbf{Q}=\begin{bmatrix}
  \rho  \\
  \rho u \\
  \rho v  \\
  \rho w  \\
  \rho E  \\
  \end{bmatrix}
  \quad 
  \mathbf{E}=\begin{bmatrix}
  \rho u \\
  \rho uu+p \\
  \rho uv  \\
  \rho uw  \\
  \rho uH  \\
  \end{bmatrix}
  \quad 
  \mathbf{F}=\begin{bmatrix}
  \rho v \\
  \rho vu \\
  \rho vv+p  \\
  \rho vw  \\
  \rho vH  \\
  \end{bmatrix}
  \quad 
  \mathbf{G}=\begin{bmatrix}
  \rho w \\
  \rho wu \\
  \rho wv  \\
  \rho ww+p  \\
  \rho wH  \\
  \end{bmatrix}
  \end{align}

:math:`E` is the specific total energy, and :math:`H` is the specific total enthalpy

.. math::
  E=\frac{1}{\gamma-1} \frac{p}{\rho}+\frac{1}{2} (u^{2}+v^{2}+w^{2})=\frac{1}{\gamma-1} \frac{p}{\rho}+\frac{1}{2} \mathbf{v}^{2}  

.. math::
  H=E+\frac{p}{\rho}
  
-

.. math::   
  \mathbf{E}_{v}=\begin{bmatrix}
  0 \\
  \tau_{xx} \\
  \tau_{yx}  \\
  \tau_{zx}  \\
  \tau_{vx}-q_{x}\\
  \end{bmatrix}
  \quad
  \mathbf{F}_{v}=\begin{bmatrix}
  0 \\
  \tau_{xy} \\
  \tau_{yy}  \\
  \tau_{zy}  \\
  \tau_{vy}-q_{y} \\
  \end{bmatrix}
  \quad
  \mathbf{G}_{v}=\begin{bmatrix}
  0 \\
  \tau_{xz} \\
  \tau_{yz}  \\
  \tau_{zz}  \\
  \tau_{vz}-q_{z} \\
  \end{bmatrix}


-

.. math::   
  \begin{align}
  \tau_{vx}=\tau_{xx}u+\tau_{xy}v+\tau_{xz}w\\
  \tau_{vy}=\tau_{yx}u+\tau_{yy}v+\tau_{yz}w\\
  \tau_{vz}=\tau_{zx}u+\tau_{zy}v+\tau_{zz}w\\
  \end{align}  
  
-

.. math::  
  \mathbf{q}=\begin{bmatrix}
  q_{x}\\
  q_{y}\\
  q_{z}
  \end{bmatrix}=\begin{bmatrix}
  -k\cfrac{\partial T}{\partial x}\\
  -k\cfrac{\partial T}{\partial y}\\
  -k\cfrac{\partial T}{\partial z}
  \end{bmatrix}  
  
The heat conductivity :math:`\kappa` can be evaluated through the viscosity coefficient :math:`\mu` by utilizing the definition of the Prandtl number :math:`Pr`,

.. math::  
  Pr=\frac{c_{p}\mu }{\kappa }=\frac{\gamma R \mu}{\kappa (\gamma -1)}\Longrightarrow \kappa= \frac{\gamma R \mu}{Pr(\gamma -1)}\\
  
viscous stress tensor:

.. math::
  \boldsymbol{\tau} = \lambda (\text{div }\mathbf{v})\mathbf{I}+\mu[(\text{grad }\mathbf{v})+(\text{grad }\mathbf{v})^{\text{T}}]
  
-

.. math::  
  \boldsymbol\tau =\begin{bmatrix}
  \tau_{xx}& \tau_{xy} & \tau_{xz}\\
  \tau_{yx}& \tau_{yy} & \tau_{yz}\\
  \tau_{zx}& \tau_{zy} & \tau_{zz}\\
  \end{bmatrix}

-

.. math:: 
  \text{div }\mathbf{v}=\cfrac{\partial u}{\partial x}+\cfrac{\partial v}{\partial y}+\cfrac{\partial w}{\partial z}
  
-

.. math:: 
  \lambda (\text{div }\mathbf{v})\mathbf{I}=\lambda \begin{bmatrix}
  \cfrac{\partial u}{\partial x}+\cfrac{\partial v}{\partial y}+\cfrac{\partial w}{\partial z}& 0 & 0\\
  0& \cfrac{\partial u}{\partial x}+\cfrac{\partial v}{\partial y}+\cfrac{\partial w}{\partial z} & 0\\
  0& 0 & \cfrac{\partial u}{\partial x}+\cfrac{\partial v}{\partial y}+\cfrac{\partial w}{\partial z}\\
  \end{bmatrix}
  
-

.. math:: 
  \lambda (\text{div }\mathbf{v})\mathbf{I}=\lambda \begin{bmatrix}
  \text{div }\mathbf{v}& 0 & 0\\
  0& \text{div }\mathbf{v} & 0\\
  0& 0 & \text{div }\mathbf{v}\\
  \end{bmatrix}  
  
-

.. math:: 
  \text{grad }\mathbf{v}=[\nabla \mathbf{v}]^{\text T}=\begin{bmatrix}
  \cfrac{\partial u}{\partial x}& \cfrac{\partial v}{\partial x} & \cfrac{\partial w}{\partial x}\\
  \cfrac{\partial u}{\partial y}& \cfrac{\partial v}{\partial y} & \cfrac{\partial w}{\partial y}\\
  \cfrac{\partial u}{\partial z}& \cfrac{\partial v}{\partial z} & \cfrac{\partial w}{\partial z}\\
  \end{bmatrix}^{\text T} = \begin{bmatrix}
  \cfrac{\partial u}{\partial x}& \cfrac{\partial u}{\partial y} & \cfrac{\partial u}{\partial z}\\
  \cfrac{\partial v}{\partial x}& \cfrac{\partial v}{\partial y} & \cfrac{\partial v}{\partial z}\\
  \cfrac{\partial w}{\partial x}& \cfrac{\partial w}{\partial y} & \cfrac{\partial w}{\partial z}\\
  \end{bmatrix}    
  
-

.. math:: 
  (\text{grad }\mathbf{v})^{\text{T}}=[\nabla \mathbf{v}]=\begin{bmatrix}
  \cfrac{\partial u}{\partial x}& \cfrac{\partial v}{\partial x} & \cfrac{\partial w}{\partial x}\\
  \cfrac{\partial u}{\partial y}& \cfrac{\partial v}{\partial y} & \cfrac{\partial w}{\partial y}\\
  \cfrac{\partial u}{\partial z}& \cfrac{\partial v}{\partial z} & \cfrac{\partial w}{\partial z}\\
  \end{bmatrix}    
  
-

.. math:: 
  \mu[(\text{grad }\mathbf{v})+(\text{grad }\mathbf{v})^{\text{T}}]=
  \mu([\nabla \mathbf{v}]^{\text{T}}+[\nabla \mathbf{v}])=
  \mu\begin{bmatrix}
  \cfrac{\partial u}{\partial x}+\cfrac{\partial u}{\partial x}& \cfrac{\partial u}{\partial y}+\cfrac{\partial v}{\partial x} & \cfrac{\partial u}{\partial z}+\cfrac{\partial w}{\partial x}\\
  \cfrac{\partial v}{\partial x}+\cfrac{\partial u}{\partial y}& \cfrac{\partial v}{\partial y}+\cfrac{\partial v}{\partial y} & \cfrac{\partial v}{\partial z}+\cfrac{\partial w}{\partial y}\\
  \cfrac{\partial w}{\partial x}+\cfrac{\partial u}{\partial z}& \cfrac{\partial w}{\partial y}+\cfrac{\partial v}{\partial z} & \cfrac{\partial w}{\partial z}+\cfrac{\partial w}{\partial z}\\
  \end{bmatrix}     
  

-

.. math::  
  \begin{align}
  \tau_{xx} & = \lambda \left ( \cfrac{\partial u}{\partial x}+
                            \cfrac{\partial v}{\partial y}+
                            \cfrac{\partial w}{\partial z} \right ) +
                     2\mu \cfrac{\partial u}{\partial x}\\
  \tau_{yy} & = \lambda \left ( \cfrac{\partial u}{\partial x}+
                            \cfrac{\partial v}{\partial y}+
                            \cfrac{\partial w}{\partial z} \right ) +
                     2\mu \cfrac{\partial v}{\partial y}\\
  \tau_{zz} & = \lambda \left ( \cfrac{\partial u}{\partial x}+
                            \cfrac{\partial v}{\partial y}+
                            \cfrac{\partial w}{\partial z} \right ) +
                     2\mu \cfrac{\partial w}{\partial z}\\
  \end{align}
  
-

.. math:: 
  \begin{align}
  \tau_{xy} & = \mu \left ( \cfrac{\partial u}{\partial y}+
                            \cfrac{\partial v}{\partial x}\right )
  \quad
  \tau_{yx}  = \mu \left ( \cfrac{\partial v}{\partial x}+
                            \cfrac{\partial u}{\partial y}\right )\\
  \tau_{xz} & = \mu \left ( \cfrac{\partial u}{\partial z}+
                            \cfrac{\partial w}{\partial x}\right )
  \quad
  \tau_{zx}  = \mu \left ( \cfrac{\partial w}{\partial x}+
                            \cfrac{\partial u}{\partial z}\right )\\
  \tau_{yz} & = \mu \left ( \cfrac{\partial v}{\partial z}+
                            \cfrac{\partial w}{\partial y}\right )
  \quad
  \tau_{zy}  = \mu \left ( \cfrac{\partial w}{\partial y}+
                            \cfrac{\partial v}{\partial z}\right )\\
  \end{align}  
  
-

.. math:: 
  \tau_{xx}+\tau_{yy}+\tau_{zz}=(3\lambda+2\mu) \left ( \cfrac{\partial u}{\partial x}+
                            \cfrac{\partial v}{\partial y}+
                            \cfrac{\partial w}{\partial z} \right ) 
  =(3\lambda+2\mu)\text{div }\mathbf{v}=(3\lambda+2\mu)(\nabla \cdot \mathbf{v}) 
  
Stokes' hypothesis states that the bulk viscosity of a Newtonian fluid can be set to zero. 

.. math::  
  3\lambda +2\mu = 0\Longrightarrow \lambda=-\cfrac{2}{3} \mu
  
-
  
.. math:: 
  \tau_{xx}+\tau_{yy}+\tau_{zz}=(3\lambda+2\mu) \left ( \cfrac{\partial u}{\partial x}+
                            \cfrac{\partial v}{\partial y}+
                            \cfrac{\partial w}{\partial z} \right )=0  
  
-
  
.. math::  
  \begin{align}
  \tau_{xx} & = \frac{2}{3} \mu\left ( 2 \frac{\partial u}{\partial x}- \frac{\partial v}{\partial y}-\frac{\partial w}{\partial z}\right )\\
  \tau_{yy} & = \frac{2}{3} \mu\left ( 2 \frac{\partial v}{\partial y}- \frac{\partial w}{\partial z}-\frac{\partial u}{\partial x}\right )\\
  \tau_{zz} & = \frac{2}{3} \mu\left ( 2 \frac{\partial w}{\partial z}- \frac{\partial u}{\partial x}-\frac{\partial v}{\partial y}\right )\\
  \end{align}  
  
The stress tensor

.. math::  
  \boldsymbol\sigma =-p\mathbf{I}+\boldsymbol{\tau}

-

.. math::  
  \sigma_{ij}=-p\delta_{ij}+\mu \left ( \cfrac{\partial u_{i}}{\partial x_{j}}+ \cfrac{\partial u_{j}}{\partial x_{i}} \right )+\delta_{ij}\lambda  \nabla \cdot \mathbf{v}  
  
total stress tensor- Cauchy stress tensor

.. math::  
  \boldsymbol\sigma =\begin{bmatrix}
  \sigma_{xx}& \sigma_{xy} & \sigma_{xz}\\
  \sigma_{yx}& \sigma_{yy} & \sigma_{yz}\\
  \sigma_{zx}& \sigma_{zy} & \sigma_{zz}\\
  \end{bmatrix}
  
the deviatoric or viscous stress tensor.  

.. math::  
  \boldsymbol\tau =\begin{bmatrix}
  \tau_{xx}& \tau_{xy} & \tau_{xz}\\
  \tau_{yx}& \tau_{yy} & \tau_{yz}\\
  \tau_{zx}& \tau_{zy} & \tau_{zz}\\
  \end{bmatrix}
  
-
  
.. math::  
  \begin{align}
  \boldsymbol\sigma & = -\begin{bmatrix}
  p& 0 & 0\\
  0& p & 0\\
  0& 0 & p\\
  \end{bmatrix}+
  \begin{bmatrix}
  \tau_{xx}& \tau_{xy} & \tau_{xz}\\
  \tau_{yx}& \tau_{yy} & \tau_{yz}\\
  \tau_{zx}& \tau_{zy} & \tau_{zz}\\
  \end{bmatrix}
  \end{align}=-p\mathbf{I}+\boldsymbol\tau 
  
-
  
.. math::  
  \boldsymbol\sigma = 
  \begin{bmatrix}
  \tau_{xx}-p& \tau_{xy} & \tau_{xz}\\
  \tau_{yx}& \tau_{yy}-p & \tau_{yz}\\
  \tau_{zx}& \tau_{zy} & \tau_{zz}-p\\
  \end{bmatrix}
  
  
-
  
.. math::  
  \begin{align}
  \sigma_{xx}&=\tau_{xx}-p\\
  \sigma_{yy}&=\tau_{yy}-p\\
  \sigma_{zz}&=\tau_{zz}-p\\
  \end{align}
  
-
  
.. math::  
  \begin{align}
  p & = -\frac{1}{3}[ (\sigma_{xx}+\sigma_{yy}+\sigma_{zz})-(\tau_{xx}+\tau_{yy}+\tau_{zz})]\\
  & = -\frac{1}{3}(\sigma_{xx}+\sigma_{yy}+\sigma_{zz})
  \end{align}
  
-
  
.. math:: 
  \text{div }\boldsymbol\tau=\nabla \cdot (\boldsymbol{\tau}^{\text{T}})=\cfrac{\partial \tau_{ij} }{\partial x_{j}}=
  \begin{bmatrix}
  \cfrac{\partial \tau_{11} }{\partial x_{1}}+
  \cfrac{\partial \tau_{12} }{\partial x_{2}}+
  \cfrac{\partial \tau_{13} }{\partial x_{3}}\\
  \cfrac{\partial \tau_{21} }{\partial x_{1}}+
  \cfrac{\partial \tau_{22} }{\partial x_{2}}+
  \cfrac{\partial \tau_{23} }{\partial x_{3}}\\
  \cfrac{\partial \tau_{31} }{\partial x_{1}}+
  \cfrac{\partial \tau_{32} }{\partial x_{2}}+
  \cfrac{\partial \tau_{33} }{\partial x_{3}}\\
  \end{bmatrix}
  
-
  
.. math:: 
  \text{div }\boldsymbol\tau=\nabla \cdot (\boldsymbol{\tau}^{\text{T}})=\cfrac{\partial \tau_{ij} }{\partial x_{j}}=
  \begin{bmatrix}
  \cfrac{\partial \tau_{xx} }{\partial x}+
  \cfrac{\partial \tau_{xy} }{\partial y}+
  \cfrac{\partial \tau_{xz} }{\partial z}\\
  \cfrac{\partial \tau_{yx} }{\partial x}+
  \cfrac{\partial \tau_{yy} }{\partial y}+
  \cfrac{\partial \tau_{yz} }{\partial z}\\
  \cfrac{\partial \tau_{zx} }{\partial x}+
  \cfrac{\partial \tau_{zy} }{\partial y}+
  \cfrac{\partial \tau_{zz} }{\partial z}\\
  \end{bmatrix}


  
-
  
.. math::   
  \begin{align}
  \text{div }\boldsymbol\tau & = \nabla \cdot (\boldsymbol{\tau}^{\text{T}})
  = \cfrac{\partial \tau_{ij} }{\partial x_{j}} \\
  & = \left ( \cfrac{\partial \tau_{xx} }{\partial x}+
  \cfrac{\partial \tau_{xy} }{\partial y}+
  \cfrac{\partial \tau_{xz} }{\partial z} \right )\mathbf{i}\\
  &+  \left (  \cfrac{\partial \tau_{yx} }{\partial x}+
  \cfrac{\partial \tau_{yy} }{\partial y}+
  \cfrac{\partial \tau_{yz} }{\partial z}\\ \right )\mathbf{j}\\
  &+ \left (  \cfrac{\partial \tau_{zx} }{\partial x}+
  \cfrac{\partial \tau_{zy} }{\partial y}+
  \cfrac{\partial \tau_{zz} }{\partial z}\ \right )\mathbf{k}
  \end{align}
  
-

.. math::
  [\boldsymbol{\tau}\cdot \mathbf{v}]=
  \begin{bmatrix}
    {\tau}_{xx}& {\tau}_{xy} & {\tau}_{xz}\\
    {\tau}_{yx}& {\tau}_{yy} & {\tau}_{yz}\\
    {\tau}_{zx}& {\tau}_{zy} & {\tau}_{zz}\\
  \end{bmatrix}
  \begin{bmatrix}
    u\\ v\\  w\\
  \end{bmatrix}
  =\begin{bmatrix}
    {\tau}_{xx}u+{\tau}_{xy}v+{\tau}_{xz}w\\
    {\tau}_{yx}u+{\tau}_{yy}v+{\tau}_{yz}w\\
    {\tau}_{zx}u+{\tau}_{zy}v+{\tau}_{zz}w\\
  \end{bmatrix}
  
-

.. math::  
  \begin{align}
  [\boldsymbol\tau \cdot \mathbf{v}]
  &=(\tau_{xx}u+\tau_{xy}v+\tau_{xz}w)\mathbf{i}\\
  &+(\tau_{yx}u+\tau_{yy}v+\tau_{yz}w)\mathbf{j}\\
  &+(\tau_{zx}u+\tau_{zy}v+\tau_{zz}w)\mathbf{k}
  \end{align}

-

.. math:: 
  \begin{align}
  \text{div }[\boldsymbol\tau \cdot \mathbf{v}]&=\nabla \cdot [\boldsymbol\tau \cdot \mathbf{v}]\\
  &=\cfrac{\partial(\tau_{xx}u+\tau_{xy}v+\tau_{xz}w) }{\partial x}\\
  &+\cfrac{\partial(\tau_{yx}u+\tau_{yy}v+\tau_{yz}w) }{\partial y}\\
  &+\cfrac{\partial(\tau_{zx}u+\tau_{zy}v+\tau_{zz}w) }{\partial z}\\
  \end{align}  
  
Conservative form of the Navier-Stokes equations

.. math:: 
  \begin{align}
  \cfrac{\partial \rho}{\partial t}+\text{div }(\rho\mathbf{v})=0\\
  \cfrac{\partial (\rho\mathbf{v})}{\partial t}+\text{div }(\rho\mathbf{v}\otimes\mathbf{v})=\text{div }\boldsymbol\sigma\\
  \cfrac{\partial (\rho E)}{\partial t}+\text{div }(\rho\mathbf{v}H)=\text{div }(\boldsymbol\tau\cdot\mathbf{v})-\text{div }\mathbf{q}\\
  \end{align}
  
-

.. math:: 
  \mathbf{vv}\equiv \mathbf{v\otimes v}=[\mathbf{v}][\mathbf{v}]^{\text{T}}=\begin{bmatrix}
  u\\v\\w
  \end{bmatrix}\begin{bmatrix}
   u& v &w
  \end{bmatrix}=\begin{bmatrix}
  uu &uv  &uw \\
  vu &vv  &vw \\
  wu &wv  &ww \\
  \end{bmatrix}   

-

.. math:: 
  \text{div }(\mathbf{vv})\equiv \text{div }(\mathbf{v\otimes v}) = \text{div }(\mathbf{F})  
  
-

.. math::
  \mathbf{F}=\begin{bmatrix}
  uu &uv  &uw \\
  vu &vv  &vw \\
  wu &wv  &ww \\
  \end{bmatrix} 
  
-

.. math::  
  \text{div}\mathbf{F} = \nabla \cdot (\mathbf{F}^{\text T})=
  \begin{bmatrix}
   \cfrac{\partial {F_{xx}}}{\partial x}
  +\cfrac{\partial {F_{xy}}}{\partial y}
  +\cfrac{\partial {F_{xz}}}{\partial z}\\
   \cfrac{\partial {F_{yx}}}{\partial x}
  +\cfrac{\partial {F_{yy}}}{\partial y}
  +\cfrac{\partial {F_{yz}}}{\partial z}\\
   \cfrac{\partial {F_{zx}}}{\partial x}
  +\cfrac{\partial {F_{zy}}}{\partial y}
  +\cfrac{\partial {F_{zz}}}{\partial z}\\
  \end{bmatrix}  =
  \begin{bmatrix}
   \cfrac{\partial {(uu)}}{\partial x}
  +\cfrac{\partial {(uv)}}{\partial y}
  +\cfrac{\partial {(uw)}}{\partial z}\\
   \cfrac{\partial {(vu)}}{\partial x}
  +\cfrac{\partial {(vv)}}{\partial y}
  +\cfrac{\partial {(vw)}}{\partial z}\\
   \cfrac{\partial {(wu)}}{\partial x}
  +\cfrac{\partial {(wv)}}{\partial y}
  +\cfrac{\partial {(ww)}}{\partial z}\\
  \end{bmatrix}    
  
-

.. math:: 
  \begin{align}
  \text{div}\boldsymbol{\sigma}  = \nabla \cdot [\boldsymbol{\sigma}]^{\text T} & = \begin{bmatrix}
   \cfrac{\partial {{\sigma}_{xx}}}{\partial x}
  +\cfrac{\partial {{\sigma}_{xy}}}{\partial y}
  +\cfrac{\partial {{\sigma}_{xz}}}{\partial z}\\
   \cfrac{\partial {{\sigma}_{yx}}}{\partial x}
  +\cfrac{\partial {{\sigma}_{yy}}}{\partial y}
  +\cfrac{\partial {{\sigma}_{yz}}}{\partial z}\\
   \cfrac{\partial {{\sigma}_{zx}}}{\partial x}
  +\cfrac{\partial {{\sigma}_{zy}}}{\partial y}
  +\cfrac{\partial {{\sigma}_{zz}}}{\partial z}\\
  \end{bmatrix} \\& = \begin{bmatrix}
   \cfrac{\partial {({\tau}_{xx}-p)}}{\partial x}
  +\cfrac{\partial {{\tau}_{xy}}}{\partial y}
  +\cfrac{\partial {{\tau}_{xz}}}{\partial z}\\
   \cfrac{\partial {{\tau}_{yx}}}{\partial x}
  +\cfrac{\partial {({\tau}_{yy}-p})}{\partial y}
  +\cfrac{\partial {{\tau}_{yz}}}{\partial z}\\
   \cfrac{\partial {{\tau}_{zx}}}{\partial x}
  +\cfrac{\partial {{\tau}_{zy}}}{\partial y}
  +\cfrac{\partial {({\tau}_{zz}-p)}}{\partial z}\\
  \end{bmatrix}\\
  & = \begin{bmatrix}
   \cfrac{\partial {{\tau}_{xx}}}{\partial x}
  +\cfrac{\partial {{\tau}_{xy}}}{\partial y}
  +\cfrac{\partial {{\tau}_{xz}}}{\partial z}\\
   \cfrac{\partial {{\tau}_{yx}}}{\partial x}
  +\cfrac{\partial {{\tau}_{yy}}}{\partial y}
  +\cfrac{\partial {{\tau}_{yz}}}{\partial z}\\
   \cfrac{\partial {{\tau}_{zx}}}{\partial x}
  +\cfrac{\partial {{\tau}_{zy}}}{\partial y}
  +\cfrac{\partial {{\tau}_{zz}}}{\partial z}\\
  \end{bmatrix}-
  \begin{bmatrix}
  \cfrac{\partial {p}}{\partial x}\\
  \cfrac{\partial {p}}{\partial y}\\
  \cfrac{\partial {p}}{\partial z}\\
  \end{bmatrix}
  \end{align}  
  
-

.. math:: 
  \text{div }\boldsymbol{\sigma}  = \nabla \cdot [\boldsymbol{\sigma}]^{\text T}
  =\text{div }\boldsymbol{\tau}-\text{grad }p
  =\text{div }\boldsymbol{\tau}-\nabla p
  =\nabla \cdot [\boldsymbol{\tau}]^{\text T}-\nabla p
 
-

.. math:: 
  \begin{align}
  \text{div }\mathbf{q}  = \nabla \cdot\mathbf{q} & = \
  \begin{bmatrix}
  \cfrac{\partial {q}}{\partial x}\\
  \cfrac{\partial {q}}{\partial y}\\
  \cfrac{\partial {q}}{\partial z}\\
  \end{bmatrix}
  \end{align} 
  
Primitive form of the Navier-Stokes equations

.. math:: 
  \begin{align}
  \cfrac{\text{d} \rho}{\text{d} t}+\rho\text{ div }\mathbf{v} & = 0\\
  \rho\cfrac{\text{d} \mathbf{v}}{\text{d} t}=\text{div }\boldsymbol\sigma&=\text{div }\boldsymbol\tau-\text{grad }p\\
  \cfrac{\text{d} p}{\text{d} t}+\gamma p\text{ div }\mathbf{v}&=(\gamma-1)[\boldsymbol\tau:\text{grad }\mathbf{v}-\text{div }\mathbf{q}]\\
  \end{align}
  
-

.. math:: 
  \begin{align}
  \cfrac{\text{d} \alpha}{\text{d} t} & = \cfrac{\partial \alpha}{\partial t}+u\cfrac{\partial \alpha}{\partial x}+v\cfrac{\partial \alpha}{\partial y}+w\cfrac{\partial \alpha}{\partial z}\\
  &= \cfrac{\partial \alpha}{\partial t}+\mathbf{v}\cdot \text{ grad } \alpha\\
  &= \cfrac{\partial \alpha}{\partial t}+\mathbf{v}\cdot \nabla \alpha\\
  \end{align}
  
-

.. math:: 
  \text{div }(\phi\mathbf{v})=\phi\text{ div }\mathbf{v}+\mathbf{v}\cdot \text{ grad }\phi
  
-

.. math:: 
  \text{div }(\rho\mathbf{v})=\rho\text{ div }\mathbf{v}+\mathbf{v}\cdot \text{ grad }\rho 

-

.. math:: 
  \cfrac{\text{d} \rho}{\text{d} t}= \cfrac{\partial \rho}{\partial t}+\mathbf{v}\cdot \text{ grad } \rho
  
-

.. math::
  \begin{align}
  \cfrac{\partial \rho}{\partial t}+\text{div }(\rho\mathbf{v}) & = \cfrac{\partial \rho}{\partial t}+\rho\text{ div }\mathbf{v}+\mathbf{v}\cdot \text{ grad }\rho \\
   &= \cfrac{\text{d} \rho}{\text{d} t}+\rho\text{ div }\mathbf{v}
  \end{align} 

-

.. math::
  \begin{align}
  \cfrac{\text{d} u}{\text{d} t} & = \cfrac{\partial u}{\partial t}+\mathbf{v}\cdot \text{ grad } u\\
  \cfrac{\text{d} v}{\text{d} t} & = \cfrac{\partial v}{\partial t}+\mathbf{v}\cdot \text{ grad } v\\
  \cfrac{\text{d} w}{\text{d} t} & = \cfrac{\partial w}{\partial t}+\mathbf{v}\cdot \text{ grad } w\\
  \end{align}  
  
-

.. math::  
  \begin{align}
  \mathbf{v}\cdot \text{ grad } u & = u\cfrac{\partial u}{\partial x}+v\cfrac{\partial u}{\partial y}+w\cfrac{\partial u}{\partial z}\\
  \mathbf{v}\cdot \text{ grad } v & = u\cfrac{\partial v}{\partial x}+v\cfrac{\partial v}{\partial y}+w\cfrac{\partial v}{\partial z}\\
  \mathbf{v}\cdot \text{ grad } w & = u\cfrac{\partial w}{\partial x}+v\cfrac{\partial w}{\partial y}+w\cfrac{\partial w}{\partial z}\\
  \end{align}  
  
-

.. math::   
  (\text{grad }\mathbf{v})^{\text{T}}=[\nabla \mathbf{v}]=\begin{bmatrix}
  \cfrac{\partial u}{\partial x}& \cfrac{\partial v}{\partial x} & \cfrac{\partial w}{\partial x}\\
  \cfrac{\partial u}{\partial y}& \cfrac{\partial v}{\partial y} & \cfrac{\partial w}{\partial y}\\
  \cfrac{\partial u}{\partial z}& \cfrac{\partial v}{\partial z} & \cfrac{\partial w}{\partial z}\\
  \end{bmatrix}  
  
-

.. math::   
  \begin{align}
  [\mathbf{v}^{\text{T}}][(\text{grad }\mathbf{v})^{\text{T}}] & = [\mathbf{v}^{\text{T}}][\nabla \mathbf{v}]  = \begin{bmatrix}
  u&v  &w
  \end{bmatrix}
  \begin{bmatrix}
  \cfrac{\partial u}{\partial x}& \cfrac{\partial v}{\partial x} & \cfrac{\partial w}{\partial x}\\
  \cfrac{\partial u}{\partial y}& \cfrac{\partial v}{\partial y} & \cfrac{\partial w}{\partial y}\\
  \cfrac{\partial u}{\partial z}& \cfrac{\partial v}{\partial z} & \cfrac{\partial w}{\partial z}\\
  \end{bmatrix}\\
  &=\begin{bmatrix}
  u\cfrac{\partial u}{\partial x}+v\cfrac{\partial u}{\partial y}+w\cfrac{\partial u}{\partial z}\\
  u\cfrac{\partial v}{\partial x}+v\cfrac{\partial v}{\partial y}+w\cfrac{\partial v}{\partial z}\\
  u\cfrac{\partial w}{\partial x}+v\cfrac{\partial w}{\partial y}+w\cfrac{\partial w}{\partial z}\\
  \end{bmatrix}^{\text{T}}
  \end{align}
  
-

.. math::  
  (\mathbf{A}\mathbf{B})^{\text{T}}=\mathbf{B}^{\text{T}}\mathbf{A}^{\text{T}}  
  
  
-

.. math:: 
  \begin{align}
  [(\text{grad }\mathbf{v})][\mathbf{v}] & = [\nabla \mathbf{v}]^{\text{T}}[\mathbf{v}]  =
  \begin{bmatrix}
  \cfrac{\partial u}{\partial x}& \cfrac{\partial u}{\partial y} & \cfrac{\partial u}{\partial y}\\
  \cfrac{\partial v}{\partial x}& \cfrac{\partial v}{\partial y} & \cfrac{\partial v}{\partial y}\\
  \cfrac{\partial w}{\partial x}& \cfrac{\partial w}{\partial y} & \cfrac{\partial w}{\partial y}\\
  \end{bmatrix}
  \begin{bmatrix}
  u\\v\\w\\
  \end{bmatrix}
  \\
  &=\begin{bmatrix}
  u\cfrac{\partial u}{\partial x}+v\cfrac{\partial u}{\partial y}+w\cfrac{\partial u}{\partial z}\\
  u\cfrac{\partial v}{\partial x}+v\cfrac{\partial v}{\partial y}+w\cfrac{\partial v}{\partial z}\\
  u\cfrac{\partial w}{\partial x}+v\cfrac{\partial w}{\partial y}+w\cfrac{\partial w}{\partial z}\\
  \end{bmatrix}
  \end{align}
  
-

.. math::
  \begin{align}
  \cfrac{\text{d} \mathbf{v}}{\text{d} t} & = \cfrac{\partial \mathbf{v}}{\partial t}+[(\text{grad }\mathbf{v})][\mathbf{v}]\\
  \cfrac{\text{d} \mathbf{v}}{\text{d} t} & = \cfrac{\partial \mathbf{v}}{\partial t}+[\nabla \mathbf{v}]^{\text{T}}[\mathbf{v}] \\
  \cfrac{\text{d} \mathbf{v}}{\text{d} t} & = \cfrac{\partial \mathbf{v}}{\partial t}+ (\mathbf{v}\cdot \nabla)\mathbf{v} \\
  \cfrac{\text{d} \boldsymbol{\alpha}}{\text{d} t} & = \cfrac{\partial \boldsymbol{\alpha}}{\partial t}+ (\mathbf{v}\cdot \nabla)\boldsymbol{\alpha} \\
  \end{align} 
  
 
-

.. math::
  \begin{align}
   (\mathbf{a}\otimes \mathbf{b})\cdot \mathbf{c}&=\mathbf{a}(\mathbf{b}\cdot\mathbf{c})\\
  \text{div }(\mathbf{a}\otimes \mathbf{b}) & = (\text{grad }\mathbf{a})\cdot \mathbf{b}+\mathbf{a}\text{ div }\mathbf{b}\\
  \text{div }(\phi \mathbf{T}) & = \mathbf{T}\cdot (\text{grad }\phi)+\phi\text{ div }\mathbf{T}\\
  \text{div }(\phi (\mathbf{a}\otimes \mathbf{b})) & = (\mathbf{a}\otimes \mathbf{b})\cdot (\text{grad }\phi)+\phi\text{ div }(\mathbf{a}\otimes \mathbf{b})\\
   (\mathbf{a}\otimes \mathbf{b})\cdot (\text{grad }\phi)&=\mathbf{a}(\mathbf{b}\cdot(\text{grad }\phi))
  \end{align}
  
-

.. math::
  \begin{align}
  \text{div }(\rho(\mathbf{v}\otimes \mathbf{v})) & = (\mathbf{v}\otimes \mathbf{v})\cdot (\text{grad }\rho)+\rho\text{ div }(\mathbf{a}\otimes \mathbf{b})\\
  \text{div }(\rho(\mathbf{v}\otimes \mathbf{v})) & = {\mathbf{v}}(\mathbf{v}\cdot (\text{grad }\rho))+\rho\text{ div }(\mathbf{v}\otimes \mathbf{v})\\
  \end{align}
  
-

.. math::
  \begin{array}{c}
  \cfrac{\text{d} \rho}{\text{d} t}  = \cfrac{\partial \rho}{\partial t}+\mathbf{v}\cdot \text{grad }\rho\\
  \cfrac{\text{d} \rho}{\text{d} t} - \cfrac{\partial \rho}{\partial t}=\mathbf{v}\cdot \text{grad }\rho\\
  \mathbf{v}\cdot \text{grad }\rho=\cfrac{\text{d} \rho}{\text{d} t} - \cfrac{\partial \rho}{\partial t}\\
  \end{array}  
  
-

.. math::
  \mathbf{v}(\mathbf{v}\cdot \text{grad }\rho)=\mathbf{v}\cfrac{\text{d} \rho}{\text{d} t} - \mathbf{v}\cfrac{\partial \rho}{\partial t}
  
-

.. math::
  \begin{align}
  \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t} & = \rho\cfrac{\partial \mathbf{v}}{\partial t}+\rho[(\text{grad }\mathbf{v})][\mathbf{v}]\\
  \rho\cfrac{\text{d} \mathbf{v}}{\text{d} t} & = \rho\cfrac{\partial \mathbf{v}}{\partial t}+\rho[\nabla \mathbf{v}]^{\text{T}}[\mathbf{v}] \\
  \end{align}
  
-

.. math::  
  \begin{align}
  \cfrac{\partial (\rho\mathbf{v})}{\partial t}=\rho\cfrac{\partial \mathbf{v}}{\partial t}+\mathbf{v}\cfrac{\partial \rho}{\partial t}\\
  \rho\cfrac{\partial \mathbf{v}}{\partial t}=  \cfrac{\partial (\rho\mathbf{v})}{\partial t}-\mathbf{v}\cfrac{\partial \rho}{\partial t}\\
  \end{align} 
  

-

.. math::
  \begin{align}
  &\cfrac{\partial (\rho\mathbf{v})}{\partial t}+\text{div }(\rho\mathbf{v}\otimes\mathbf{v}) \\
  =& \cfrac{\partial (\rho\mathbf{v})}{\partial t}+{\mathbf{v}}(\mathbf{v}\cdot (\text{grad }\rho))+\rho\text{ div }(\mathbf{v}\otimes \mathbf{v})\\
  =& \rho\cfrac{\partial \mathbf{v}}{\partial t}+\mathbf{v}\cfrac{\partial \rho}{\partial t}+{\mathbf{v}}(\mathbf{v}\cdot (\text{grad }\rho))+\rho\text{ div }(\mathbf{v}\otimes \mathbf{v})\\
  =& \rho\cfrac{\partial \mathbf{v}}{\partial t}+\mathbf{v}\cfrac{\partial \rho}{\partial t}+[\mathbf{v}\cfrac{\text{d} \rho}{\text{d} t} - \mathbf{v}\cfrac{\partial \rho}{\partial t}]+\rho\text{ div }(\mathbf{v}\otimes \mathbf{v})\\
  =& \rho\cfrac{\partial \mathbf{v}}{\partial t}+\mathbf{v}\cfrac{\text{d} \rho}{\text{d} t}+\rho\text{ div }(\mathbf{v}\otimes \mathbf{v})\\
  \end{align} 
  
-

.. math::  
  \begin{align}
  \rho\cfrac{\partial \mathbf{v}}{\partial t}&= \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t} -\rho[(\text{grad }\mathbf{v})][\mathbf{v}]\\
  \rho\cfrac{\partial \mathbf{v}}{\partial t}&= \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t} -\rho[\nabla \mathbf{v}]^{\text{T}}[\mathbf{v}]\\
  \end{align}
  
-

.. math::  
  \begin{align}
  &\cfrac{\partial (\rho\mathbf{v})}{\partial t}+\text{div }(\rho\mathbf{v}\otimes\mathbf{v}) \\
  =& \rho\cfrac{\partial \mathbf{v}}{\partial t}+\mathbf{v}\cfrac{\text{d} \rho}{\text{d} t}+\rho\text{ div }(\mathbf{v}\otimes \mathbf{v})\\
  =& (\rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t} -\rho[(\text{grad }\mathbf{v})][\mathbf{v}])+\mathbf{v}\cfrac{\text{d} \rho}{\text{d} t}+\rho\text{ div }(\mathbf{v}\otimes \mathbf{v})\\
  =& \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t}+\mathbf{v}\cfrac{\text{d} \rho}{\text{d} t}-\rho[(\text{grad }\mathbf{v})][\mathbf{v}]+\rho\text{ div }(\mathbf{v}\otimes \mathbf{v})\\
  \end{align}  

-

.. math::  
  \begin{align}
  \text{div }(\mathbf{v}\otimes \mathbf{v}) & = (\text{grad }\mathbf{v})\cdot \mathbf{v}+\mathbf{v}\text{ div }\mathbf{v}\\
  \rho \text{ div }(\mathbf{v}\otimes \mathbf{v}) & = \rho (\text{grad }\mathbf{v})\cdot \mathbf{v}+\rho \mathbf{v}\text{ div }\mathbf{v}\\
  \end{align}
  
-

.. math::  
  \begin{align}
  &\cfrac{\partial (\rho\mathbf{v})}{\partial t}+\text{div }(\rho\mathbf{v}\otimes\mathbf{v}) \\
  =& \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t}+\mathbf{v}\cfrac{\text{d} \rho}{\text{d} t}-\rho[(\text{grad }\mathbf{v})][\mathbf{v}]+\rho\text{ div }(\mathbf{v}\otimes \mathbf{v})\\
  =& \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t}+\mathbf{v}\cfrac{\text{d} \rho}{\text{d} t}-\rho[(\text{grad }\mathbf{v})][\mathbf{v}]+\rho (\text{grad }\mathbf{v})\cdot \mathbf{v}+\rho \mathbf{v}\text{ div }\mathbf{v}\\
  =& \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t}+\mathbf{v}\cfrac{\text{d} \rho}{\text{d} t}+\rho \mathbf{v}\text{ div }\mathbf{v}\\
  =& \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t}+\mathbf{v}(\cfrac{\text{d} \rho}{\text{d} t}+\rho \text{ div }\mathbf{v})\\
  =& \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t}+\mathbf{v}\cdot(0)\\
  =& \rho  \cfrac{\text{d} \mathbf{v}}{\text{d} t}\\
  \end{align}
  
-

.. math::   
  \mathbf{A}:\mathbf{B}=\text{tr}(\mathbf{A}^{\text{T}}\mathbf{B})
  =\text{tr}(\mathbf{A}\mathbf{B}^{\text{T}})
  =\text{tr}(\mathbf{B}^{\text{T}}\mathbf{A})
  =\text{tr}(\mathbf{B}\mathbf{A}^{\text{T}})\\  
  
-

.. math::
  \text{div }(\mathbf{T}\cdot\mathbf{v}) = \mathbf{v}\cdot(\text{div }\mathbf{T}^{\text{T}})+\text{tr}(\mathbf{T}\cdot \text{grad }\mathbf{v})  