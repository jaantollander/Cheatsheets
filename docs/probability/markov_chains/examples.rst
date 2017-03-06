Examples
========

Birth-and-Death Chains
----------------------

.. math::
   \gamma_{i+1} \pi(i + 1) = \beta_{x} \pi(i), \quad i \in 0, 1, 2,...

where

- :math:`\beta_{i} = \Pr(i, i+1)` is probability of birth
- :math:`\gamma_{i} = \Pr(i, i-1)` is probability of death
- :math:`1 - \beta_{i} - \gamma_{i}` is probability of being still

----

Branching Process (Galton-Watson)
---------------------------------

Genereting Functions

.. math::
   \phi : [-1, 1] \to \mathbb{R}

.. math::
   \phi_{Y}(s) = E(s^Y) = \sum_{k=0}^{\infty} s^{k} p(k)

For independent random variables :math:`X` and :math:`Y`

.. math::
   \phi_{X + Y}(s) = \phi_{X}(s) \phi_{Y}(s)


Expected population size

Probability of extinction: Smallest non-negative solution for

.. math::
   \phi_{Y_{1}}(s) = s


----


Constant rate :math:`\alpha`

.. math::
   P_{t}(i, j) = \sum_{n=0}^{\infty} \exp{-\alpha t} \frac{(\alpha t)^{n}}{n!} P_{*}^{n}(i, j)

----

Non-constant rate :math:`\lambda(i)\leq \alpha`

.. math::
   P_t = \sum_{n=0}^{\infty} \exp{-\alpha t} \frac{(\alpha t)^{n}}{n!} \hat{P}^{n}(i, j)

.. math::
   \hat{P}^{n}(i, j) = \frac{\lambda(i)}{\alpha} P_{*}(i, j) + \left( 1 - \frac{\lambda(i)}{\alpha} \right) I(i, j)

