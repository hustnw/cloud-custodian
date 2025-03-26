EVS - volumes auto tag user
==================================

.. code-block:: yaml

  policies:
      - name: evs-auto-tag-nwtest
        resource: huaweicloud.evs-volume
        mode:
          type: cloudtrace
          xrole: fgs_admin
          enable_lts_log: true
          default_region: sa-brazil-1
          events:
            - source: "EVS.evs"
              event: "createVolume"
              ids: "resource_id"
        filters:
          - type: value
            key: metadata.__system__encrypted
            value: "0"
        actions:
          - type: auto-tag-user
            tag: OwnerContact


