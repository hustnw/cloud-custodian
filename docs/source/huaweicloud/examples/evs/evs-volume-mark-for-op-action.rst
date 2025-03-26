EVS - Tag volumes for future action
====================================

.. code-block:: yaml

  policies:
    - name: volume-mark-for-op
      resource: huaweicloud.evs-volume
      filters:
        - type: value
          key: metadata.__system__encrypted
          value: "0"
      actions:
        - type: mark-for-op
          tag: testkey
          op: delete
          days: 4


