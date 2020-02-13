failover heartbeat
------------------
failover address doesn't use management as a backup.
        "failoverAddress": {
            "class": "FailoverUnicast",
            "address": "/Common/internal-self/address"
        },
        192.168.1.4?
        
Mirroring address
-----------------
        "mirrorAddress": {
            "class": "mirrorPrimary",
            "address": "/Common/internal-self/address"
        },
