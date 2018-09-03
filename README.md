# NM-Homework
> Spring 2017 - MSc - Amirkabir University of Technology

## Introduction
Network Management Course projects includes:

1. Netflow
2. NetXMS

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
   ovs−vsctl −− set Bridge br0 netflow=@nf −− −−id=@nf create NetFlow targets=\"10.10.10.10\"
   ```


### Netflow Collector

nProbe: An Extensible NetFlow v5/v9/IPFIX Probe for IPv4/v6.
nProbe can act as a probe, proxy and collector and you can configure it to do so.

## NetXMS
Let's use [it's docker](https://github.com/juliusloman/netxms-dockerfiles) for having lots of fun.
