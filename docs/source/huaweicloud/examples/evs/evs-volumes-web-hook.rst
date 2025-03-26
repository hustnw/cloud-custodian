EVS - Volume web hook
============================

.. code-block:: yaml

  policies:
     - name: volume-web-hook
       resource: huaweicloud.evs-volume
       actions:
         - type: webhook
           url: "https://console.huaweicloud.com/ecm/?agencyId=bf60daff45614780afd89b5df5bd58da&region=sa-brazil-1&locale=zh-cn#/evs/manager/volumelist/detail?volumeid=8c9ea2ee-3414-4dd9-b28b-8dbfa1720636"
           method: GET

