<!-- TOP -->
<div class="top">
  <img class="scenario-academy-logo" src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Gossip</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:academy@datastax.com">email</a>.</span>
  </div>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step1"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
<span class="step-count">Step 2 of 2</span>
</div>

<!-- CONTENT -->

<div class="step-title">Continue exploring gossip in the cluster</div>


✅ Terminate *node2*:
```
/workspace/ds201-lab09/node2/bin/nodetool stopdaemon
```
Wait for it to start

✅ Get the gossip information - check for *node1*:
```
/workspace/ds201-lab09/node2/bin/nodetool gossipinfo
```
<img src="https://katapod-file-store.s3.us-west-1.amazonaws.com/ds201/lab09-image03.png" />

---
**Note:** *node2*'s gossip state is still present as the node hasn’t been removed from the cluster; however its heartbeat no longer increases.

---

✅ Restart *node2*:
```
/workspace/ds201-lab09/node2/bin/cassandra
```

✅ Get the gossip information again for either node:
```
/workspace/ds201-lab09/node2/bin/nodetool gossipinfo
```
<img src="https://katapod-file-store.s3.us-west-1.amazonaws.com/ds201/lab09-image04.png" />

Observe how the generation value is the same as before for *node1*, but is now different for *node2* after it has restarted. The heartbeat value has also reset for *node2*.

✅ Start cqlsh to connect to node1:
```
/workspace/ds201-lab09/node1/bin/cqlsh
```
✅ Execute the following query on the *system.peers* table:
```
SELECT peer, data_center, host_id, rack, release_version, rpc_address, schema_version FROM system.peers;
```
The *system.peers* table stores the same gossip data about a node's peers. Check and make sure that the values here are some of the same values you saw from the `nodetool gossipinfo` command. Note that a node does not store a row of peer data for itself; that can be found in the `system.local` table.



<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
  <a href='command:katapod.loadPage?[{"step":"step1"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
</div>
