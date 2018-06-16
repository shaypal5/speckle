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
    "speckle_distribution_name": "binomial",
    "n": 43,
    "p": 0.3
  }

Specification
=============

Probability Distributions
-------------------------
