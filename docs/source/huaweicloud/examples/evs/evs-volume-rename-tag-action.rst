EVS - Create a new tag with identical value & remove old tag
============================================================

.. code-block:: yaml

  policies:
    - name: volume-rename-tag
      resource: huaweicloud.evs-volume
      filters:
        - type: value
          key: metadata.__system__encrypted
          value: "0"
      actions:
        - type: rename-tag
          old_key: testkey
          new_key: newtestkey


