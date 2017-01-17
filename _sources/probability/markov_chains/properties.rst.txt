Properties
==========

Reducibility
------------

Accessibility
^^^^^^^^^^^^^
Denoted :math:`i \to j` which means

.. math::
   \Pr(X_{n}=j\mid X_{0}=i) > 0.\,


Communicative
^^^^^^^^^^^^^
Denoted :math:`i \leftrightarrow j` and is equivalent with :math:`(i \to j) \wedge (j \to i)`.


Irreducible
^^^^^^^^^^^
Denoted :math:`i \to j, \quad \forall i, j \in S` which means that it is possible to get to any state from any state

.. math::
   \Pr(X_{n}=j\mid X_{0}=i) = P^{n}(i, j) > 0, \quad \exists t \geq 1, \quad \forall i, j \in S


Periodicity
-----------
A state :math:`i` has **period** :math:`k` if any return to state :math:`i` must occur in multiples of :math:`k` time steps. Formally defined

.. math::
   k=\gcd\{n>0:\Pr(X_{n}=i\mid X_{0}=i)>0\}

- **Aperiodic** if :math:`k = 1`
- **Periodic** if :math:`k \geq 2`

----

Every **irreducible** and **aperiodic** Markov chain has a stationary distribution.

----


Transience and Recurrence
-------------------------

Absorbing states
^^^^^^^^^^^^^^^^
A state :math:`i` is called absorbing if it is impossible to leave this state.

.. math::

   \begin{cases}
   p_{ii} = 1 \\
   p_{ij} = 0 & i \neq j
   \end{cases}


Ergodicity
----------
