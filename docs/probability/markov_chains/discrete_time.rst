Discrete-Time
=============
A discrete-time Markov chain is sequence of random variables

.. math::

   (X_t)_{t \geq 0}.

Possible values of :math:`X_i` form a finite or countable **state space** :math:`S`.


Time Homogenous Processes
-------------------------
Time-homogeneous Markov chains (or stationary Markov chains) are processes where

.. math::

   \Pr(X_{n+1}=x\mid X_{n}=y)=\Pr(X_{n}=x\mid X_{n-1}=y)\,

for all :math:`n`. The probability of the transition is independent of :math:`n`.


Markov Property
---------------

.. math::
   \Pr(X_{n+1}=x\mid X_{1}=x_{1},X_{2}=x_{2},\ldots ,X_{n}=x_{n})= \\
   \Pr(X_{n+1}=x\mid X_{n}=x_{n})

----

Transition Matrix
-----------------
For :math:`i, j \in S`

.. math::
   P(i, j) &\geq 0 \\
   \sum_{j \in S} P(i, j) &= 1

Function definition

.. math::
   P : S \times S \to [0, 1]

----

Marginal Distribution
---------------------

.. math::
   \boldsymbol{\mu}_{n}(j) = \sum_{i \in S} \boldsymbol{\mu}_{0}(i) P^{n}(i, j)

In vector form

.. math::
   \boldsymbol{\mu}_n = \boldsymbol{\mu}_0 P^{n}


----

Transition Probability
----------------------
Probability of going from state :math:`i` to :math:`j` in :math:`n` timesteps

.. math::
   \Pr(X_{n}=j\mid X_{0}=i) = P^{n}(i, j)

----

Expected Number of Visits
-------------------------

.. math::
   M_t(i, j) = \sum_{s = 0}^{t} P^{s}(i, j)

----

Limiting Distribution
---------------------
Also stationary distribution for finite Markov chains.

.. math::
   \boldsymbol{\pi}(j) = \sum_{i \in S} \boldsymbol{\pi}(i) P(i, j)

In vector form

.. math::
   \boldsymbol{\pi} = \boldsymbol{\pi} P

and

.. math::
   \sum_{i \in S} \boldsymbol{\pi}(i) = 1


Expected Number of Hits
-----------------------

.. math::
   g_n(i) = \sum_{j \in S} M_{n} (i, j) c(j)

In vector form

.. math::
   g_{n} = M_{n} c

where :math:`c(i)` is the cost of hitting node :math:`i`

----

Expected number of hits a the long run

.. math::
   g(i) = \sum_{j \in S} \boldsymbol{\pi}(j) c(j)

----

Travel Time
-----------
To group :math:`A`

.. math::
   T_A = \min\{t \geq 0 : X_{t} \in A\}

Collection of expected travel times

.. math::
   \begin{cases}
   f(i) = 1 + \sum_{y \notin A} P(i, j) f(j) & i \notin A \\
   f(i) = 0 & i \in A
   \end{cases}

smallest non-negative solution.

----

Hitting Probability
-------------------
Group :math:`A`

.. math::
   \begin{cases}
   f(i) = \sum_{y \notin A} P(i, j) f(j) & i \notin A \\
   f(i) = 1 & i \in A
   \end{cases}

smallest non-negative solution.


Reversibility
-------------
A Markov chain is said to be **reversible** if there is a probability distribution :math:`\boldsymbol{\pi}`  over its states such that

.. math::
   \boldsymbol{\pi}(i) P(i, j) = \boldsymbol{\pi}(j)P(j, i), \quad \forall x, y \in S
