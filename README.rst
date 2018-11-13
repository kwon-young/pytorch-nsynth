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

* install pytorch, scipy
* clone this repo: `git clone git@github.com:kwon-young/pytorch-nsynth.git`
* add module directory to `PYTHONPATH`: `export PYTHONPATH=pytorch-nsynth_dir:$PYTHONPATH`
* download tar.gz files from https://magenta.tensorflow.org/datasets/nsynth
* unpack archive

```python
# audio samples are loaded as an int16 numpy array
# rescale intensity range as float [-1, 1]
toFloat = transforms.Lambda(lambda x: x / np.iinfo(np.int16).max)
# use instrument_family and instrument_source as classification targets
dataset = NSynth(
"data/nsynth-test",
transform=toFloat,
blacklist_pattern=["string"],  # blacklist string instrument
categorical_field_list=["instrument_family", "instrument_source"])
loader = data.DataLoader(dataset, batch_size=32, shuffle=True)
for samples, instrument_family_target, instrument_source_target, targets \
    in loader:
print(samples.shape, instrument_family_target.shape,
      instrument_source_target.shape)
print(torch.min(samples), torch.max(samples))
```

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
