<template>
  <div class="layout">

<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <g-link class="navbar-brand" to="/">{{ $static.metadata.siteName }}</g-link>

  <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
    <div class="navbar-nav ml-auto">
      <g-link class="nav-item nav-link" to="/">Strona główna</g-link>
      <g-link class="nav-item nav-link" to="/about">O mnie</g-link>
    </div>
  </div>
</nav>


    <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}


.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}
</style>
