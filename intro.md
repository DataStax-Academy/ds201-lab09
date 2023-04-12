<!-- TOP -->
<div class="top">
  <img class="scenario-academy-logo" src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Gossip</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:academy@datastax.com">email</a>.</span>
  </div>
</div>

<!-- CONTENT -->
<main>
  <br/>
  <div class="container px-4 py-2">
    <div class="row g-4 py-2 row-cols-1 row-cols-lg-1">
      <div class="feature col div-choice">
        <div class="scenario-description">Gossip</div>
          <ul>
            <li><span class="scenario-description-attribute">Difficulty</span>: Beginner</li>
            <li><span class="scenario-description-attribute">Time</span>: 10 minutes</li>
          </ul>
          <div class="scenario-objectives">In this hands-on lab, you will:</div>
            <ul>
              <li><span class="scenario-objective">Use <i>nodetool</i> to view gossip information from different nodes</span></li>
              <li><span class="scenario-objective">Examine the gossip information stored locally in the database</span></li>
            </ul>
            <p>
            In a fully distributed system such as Cassandra there is no single repository that contains the state of all the nodes in the cluster. Clearly, such a repository would be a single point of failure. Instead, a Cassandra node uses the Gossip protocol to distribute node status amongst its peers.
            </p>
          </div>  
          <a href='command:katapod.loadPage?[{"step":"step1"}]' class="btn btn-primary btn-cassandra">
            Start the lab
          </a>
         </div>
      </div>
    </div>
  </div>
</main>