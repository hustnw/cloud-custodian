EVS - Reduce filter to group, sort, and limit volumes
============================================================

.. code-block:: yaml

  policies:
     - name: volume-reduce
       description: |
         select a 10 percent of volumes, but no more than 3.
       resource: huaweicloud.evs-volume
       filters:
         - type: reduce
           order: randomize
           limit: 3
           limit-percent: 10
