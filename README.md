# Wave Equation with Damping

The wave equation is a partial differential equation that describes the motion of waves. In one spatial dimension, it has the 
form:

<p align="center">
  <img src="https://gist.githubusercontent.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/waveeq1.png">
</p>

Where c is the propagation speed. This is a second-order partial differential equation - the highest term (in this case, all terms) contains a second partial derivative.

### Wikipedia - [Derivaton](https://en.wikipedia.org/wiki/Wave_equation#Derivation_of_the_wave_equation) of the Wave Equation

The wave equation is derived from the motion of springs; this link has a discussion.















## Analytic Solution

A method for the solution of this relatively simple PDE, seperation of variables, allows us to find a solution by assuming that the function u is the product of a function of x and a function of t:

<p align="center">
  <img src="https://gist.githubusercontent.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/seperation.png">
</p>

If we substitute into the first equation we obtain

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/seperation-step1.png">
</p>

Rearranging, we have

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/seperation-step2.png">
</p>

As this is equating functions of different variables, both sides must be qual to a constant:

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/seperation-step3a.png">
</p>

Rearranging, we find that this is a set of eigenvalue problems in which the second derivative of a function is proportional to the function itself:

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/seperation-step3b.png">
</p>

If lambda > 0, then the solutions to these ordinary differential equations are:

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/seperation-step4.png">
</p>

After lots of handwaving of the material on page three of [this](https://www.math.hmc.edu/~ajb/PCMI/lecture7.pdf), we find that a general solution is of the  form

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/step5.png">
</p>

Using multiplicative trigonemtric [identies](https://en.wikipedia.org/wiki/List_of_trigonometric_identities#Product-to-sum_and_sum-to-product_identities), this  becomes

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/step6.png">
</p>

where

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/step6-where.png">
</p>

Thus the solution is the sum of two functions, f_n and g_n, that each continuously shift in both directons along the x-axis.


















## With Damping

The version of the wave equation presented above models a system in which waves propate forever without dying out. A version of the wave equation that models "dying out" contains a term with a damping factor:

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/f908bf6ba17eb6448d308f8c16224efe6995b116/waveeqdm1.png">
</p>








This time we'll try to solve this numerically, starting with the definitions of first and second derivatives:

<p align="center">
  <img src="https://gist.github.com/chrisf2643/fe713037e0e82dcc2f429bddd1ed997a/raw/33455f10d829bc479781bdae6d6711e2cee936f0/dxforumlas.png">
</p>


