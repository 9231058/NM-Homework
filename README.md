# NM-Homework

## Introduction
Network Management Course homework

## Netflow
### Netflow Exporter
* Install OVS

   ```sh
   sudo apt install openvswitch-switch
   ```

* Create OVS

   ```sh
   # creation
   sudo ovs-vsctl add-br br0
   ```

* There are two steps involved in attaching a NetFlow monitor to a bridge:
   * defining the monitor
   * linking a bridge to monitor

   Because vSwitch is aggressive about cleaning unlinked database records,
   the definition of the NetFlow configuration should be done at the same time as its first attachment.

   ```sh
   ovs−vsctl −− set Bridge br0 netflow=@nf −− −−id=@nf create NetFlow targets=10.10.10.10
   ```


### Netflow Collector
nProbe: An Extensible NetFlow v5/v9/IPFIX Probe for IPv4/v6.
