Speckle: A specification for probability distribution serialization
###################################################################

**Speckle** is meant to be a simple specification for the serialization of probability distributions, compatible with common serialization formats.


.. contents::
.. section-numbering::


Features
========

* Human readable.
* Compatability with common serialization formats.


Examples
========

A binomial distribtuion serialized as a JSON object has the form:

.. code-block:: json

  {
    "probability_distribution_name": "binomial",
    "n": 43,
    "p": 0.3
  }

Specification
=============

General
-------

All distribution specifications can indclude the ``random seed`` parameter to increase reproducability of specific streams of samples of a distribution.


.. https://docs.scipy.org/doc/numpy-1.14.0/reference/generated/numpy.random.RandomState.html#numpy.random.RandomState
.. http://js2007.free.fr/code/index.html#RandomKit
.. https://github.com/numpy/numpy/tree/master/numpy/random/mtrand


Distribution Sets
-----------------

Any parameter can be assigned an array of values. A distribution specification is understood to specify the set of distribution given by the cartesian product of all value arrays. The case where all parameters are assigned a single value is thus understood so specify a set made of a single distribution, and thus can thought of as specifying a single distribution.


Probability Distributions
-------------------------

Bernoulli
~~~~~~~~~

* Distribution names: ``bernoulli``
* ``p`` - Probability for success/for the random variable to take a value of 1.

Binomial
~~~~~~~~

* Distribution names: ``binomial``
* ``n`` - Number of trials.
* ``p`` -  Success probability in each trial.



