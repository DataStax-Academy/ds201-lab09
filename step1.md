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
  <a href='command:katapod.loadPage?[{"step":"intro"}]'
    class="btn btn-dark navigation-top-left">⬅️ Back
  </a>
  <span class="step-count"> Step 1 of 2</span>
  <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Explore gossip in the cluster</div>

✅ Use *nodetool* to verify that both nodes are running:
```
/workspace/ds201-lab09/node1/bin/nodetool status
```

✅ Use *nodetool* to examine gossip:
```
/workspace/ds201-lab09/node1/bin/nodetool gossipinfo
```
Take note of the gossip information for both nodes as discussed in the lecture.

<img src="https://katapod-file-store.s3.us-west-1.amazonaws.com/ds201/lab09-image01.png" />

---
**Note:** Although the command retrieves the gossip info from node1, it also knows the gossip state of node2. Also take note of how the node state consists of key-values pairs as discussed in the slides.

---

✅	Run the `nodetool gossipinfo` command several more times and check how the heartbeat values changes for both nodes.

✅	Run `nodetool gossipinfo` on *node2*:
```
/workspace/ds201-lab09/node2/bin/nodetool gossipinfo
```
Verify whether the gossip information is the same as it is for *node1*, especially the status.

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
   <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>
