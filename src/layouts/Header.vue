<template>
  <div class="header-layout">
    <header class="header">
      <strong>
        <!-- <g-link to="/">{{ $static.metadata.siteName }}</g-link> -->
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about/">About Me</g-link>
        <g-link class="nav__link" to="/blog/">My Blog</g-link>
        <g-link class="nav__link" to="/contact/">Contact</g-link>
      </nav>
    </header>
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

.header-layout {
  max-width: 100%;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* margin-bottom: 20px; */
  height: 80px;
  background-color: #5BC0BE;
} 

.nav__link {
  margin-left: 10px;
  margin-right: 10px;
  color: #131200;
}
</style>
