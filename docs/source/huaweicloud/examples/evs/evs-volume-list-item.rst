EVS - Filter volumes by list item
============================================================

.. code-block:: yaml

  policies:
     - name: volume-list-item
       description: |
         filter evs disk which attr is a list, such as attachments
       resource: huaweicloud.evs-volume
       filters:
         - type: list-item
           key: attachments
           attrs:
             - type: value
               key: device
               value: /dev/vda
             - type: value
               key: server_id
               value: e8b31928-bfd4-413f-9258-43facc3e8da0



