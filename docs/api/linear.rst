Linear Classifier API
=====================


Train and Predict
^^^^^^^^^^^^^^^^^
Linear methods are methods based on
`LibLinear <https://www.csie.ntu.edu.tw/~cjlin/liblinear/>`_.
The simplest usage is::

   model = linear.train_1vsrest(train_y, train_x, options)
   predict = linear.predict_values(model, test_x)

.. See `the user guide <../guides/linear_guides.html>`_ for more details.

.. automodule:: libmultilabel.linear.linear
   :members:

.. currentmodule:: libmultilabel.linear.tree

.. autofunction:: train_tree

Preprocessor
^^^^^^^^^^^^

.. automodule:: libmultilabel.linear.preprocessor
   :members:


Load and Save Pipeline
^^^^^^^^^^^^^^^^^^^^^^

.. currentmodule:: libmultilabel.linear.utils

.. autofunction:: save_pipeline

.. autofunction:: load_pipeline

Metrics
^^^^^^^
Metrics are specified by their names in ``compute_metrics`` and ``get_metrics``.
The possible metric names are:

* ``'P@K'``, where ``K`` is a positive integer
* ``'RP@K'``, where ``K`` is a positive integer
* ``'Macro-F1'``
* ``'Micro-F1'``

.. Their definitions are given in the `user guide <https://www.csie.ntu.edu.tw/~cjlin/papers/libmultilabel/userguide.pdf>`_.

.. automodule:: libmultilabel.linear.metrics
   :members:

Grid Search with Sklearn Estimators
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. currentmodule:: libmultilabel.linear.utils

.. autoclass:: MultiLabelEstimator
   :members:

   .. automethod:: __init__

   .. automethod:: fit

   .. automethod:: predict

   .. automethod:: score

.. autoclass:: GridSearchCV
   :members:

   .. automethod:: __init__
