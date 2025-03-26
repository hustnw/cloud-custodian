EVS - Removes the specified tags from the specified volumes.
============================================================

.. code-block:: yaml

  policies:
    - name: volume-remove-tag1
      resource: huaweicloud.evs-volume
      filters:
        - type: value
          key: metadata.__system__encrypted
          value: "0"
      actions:
        - type: remove-tag
          tag_values:
            testkey1: testval1
            testkey2: testval2

  policies:
    - name: volume-remove-tag2
      resource: huaweicloud.evs-volume
      filters:
        - type: value
          key: metadata.__system__encrypted
          value: "0"
      actions:
        - type: remove-tag
          tags:
            - testkey1
            - testkey2

