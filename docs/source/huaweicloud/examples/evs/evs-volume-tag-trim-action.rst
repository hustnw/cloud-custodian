EVS - trim volume tags
========================

.. code-block:: yaml

  policies:
    - name: volume-tag-trim
      resource: huaweicloud.evs-volume
      filters:
        - type: value
          key: metadata.__system__encrypted
          value: "0"
      actions:
        - type: tag-trim
          space: 8
          preserve:
            - testkey1
            - testkey2


