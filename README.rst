==============
pytorch-nsynth
==============


.. image:: https://img.shields.io/pypi/v/pytorch_nsynth.svg
        :target: https://pypi.python.org/pypi/pytorch_nsynth

.. image:: https://img.shields.io/travis/kwon-young/pytorch_nsynth.svg
        :target: https://travis-ci.org/kwon-young/pytorch_nsynth

.. image:: https://readthedocs.org/projects/pytorch-nsynth/badge/?version=latest
        :target: https://pytorch-nsynth.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status




pytorch dataset for nsynth data


* Free software: MIT license
* Documentation: https://pytorch-nsynth.readthedocs.io.


How to use
----------

For tensorflow:

* install tensorflow
* download tfrecord files from https://magenta.tensorflow.org/datasets/nsynth
* use code in pytorch_nsynth/from_tfrecord.py

For pytorch:

* install pytorch, scipy
* download tar.gz files from https://magenta.tensorflow.org/datasets/nsynth
* unpack archive to data/
* see code in pytorch_nsynth/nsynth.py for usage

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
