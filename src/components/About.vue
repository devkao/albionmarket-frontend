<template>
  <div>
    <h2>About</h2>
    <p>Albion Market was inspired by <a href="https://github.com/gtaylor/EVE-Market-Data-Relay">EVE Market Data Relay</a> and <a href="https://github.com/theatrus/eve-central.com">eve-central.com</a>. With Albion Market relying on as many people as possible installing the client, and it is just the nice thing to do, all of the data Albion Market has is provided to others via an API. Be sure to check out the <router-link to="/api">API</router-link> page if you're into developing things and would like some market data.</p>
    <h3>Contacts</h3>
    <ul>
      <li>Albion Character: FoxFour</li>
      <li>Twitter: <a href="https://twitter.com/regnerba">@RegnerBA</a></li>
      <li>GitHub: <a href="https://github.com/regner">regner</a></li>
    </ul>
    <h3>Source Code</h3>
    <p>Along with making all of the APIs available for others to use the source code for all of components that make up Albion Market are open sourced on GitHub. Feel free to check them out, open issues, and submit PRs.</p>
    <p>The distributed client is written with Golang and relies on gopacket's pcap support. It looks for UDP packets with a specific set of bytes that identify the market packets. It then pulls out some JSON from those packets and sends the raw JSON to an HTTP ingest API. The backend is a Python Flask project that uses Postgres to store the information and exposes an HTTP API. Along with handling the ingest the backend also offers a set of APIs for getting the data from the database. The frontend is written with Vue JS and utalizes both Vue Router and VueX for routing and state management. The backend, frontend, and supporting systems (Postgres, Prometheus, etc.) are hosted in a GKE cluster (Google's hosted Kubernetes offering).</p>
    <ul>
      <li>Backend: <a href="https://github.com/Regner/albionmarket-backend">albionmarket-backend</a></li>
      <li>Frontend: <a href="https://github.com/Regner/albionmarket-frontend">albionmarket-frontend</a></li>
      <li>Client: <a href="https://github.com/Regner/albionmarket-client">albionmarket-client</a></li>
    </ul>
  </div>
</template>