EVS - Create volume tags
========================

.. code-block:: yaml

  policies:
    - name: volume-tag
      resource: huaweicloud.evs-volume
      filters:
        - type: value
          key: metadata.__system__encrypted
          value: "0"
      actions:
        - type: tag
          tags:
            testkey1: testval1
            testkey2: testval2


