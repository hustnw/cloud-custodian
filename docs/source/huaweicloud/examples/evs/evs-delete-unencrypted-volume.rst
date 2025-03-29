EVS - Delete unencrypted volumes
================================

.. code-block:: yaml

  policies:
     - name: terminate-unencrypted-evs
       description: |
         Terminate all unencrypted EVS volumes upon creation
       resource: huaweicloud.evs-volume
       filters:
         - or:
            - type: value
              key: metadata.__system__encrypted
              value: "0"
            - type: value
              key: metadata.__system__encrypted
              value: "empty"
         - type: value
           key: status
           value: available
       actions:
         - delete
