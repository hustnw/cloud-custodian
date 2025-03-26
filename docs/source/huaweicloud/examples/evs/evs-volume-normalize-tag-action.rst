EVS - Transform the value of a volume tag.
==========================================

.. code-block:: yaml

  policies:
    - name: volume-normalize-tag
      resource: huaweicloud.evs-volume
      filters:
        - type: value
          key: metadata.__system__encrypted
          value: "0"
      actions:
        - type: normalize-tag
          key: testkey
          action: upper


