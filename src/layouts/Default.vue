<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about/">About</g-link>
      </nav>
    </header>
    <slot/>

    <div class="footer">
      <p>
        Built by <g-link class="nav__link" to="/">Zach Johnson</g-link>
        find me here
        <a href="//twitter.com/notthefakezj"><i class="fab fa-twitter"></i></a>
        <a href="//linkedin.com/in/zach-johnson-5b1145127"><i class="fab fa-linkedin"></i></a>
        <a href="//instagram.com/zachaj23"><i class="fab fa-instagram"></i></a>
        <a href="//github.com/Ballcapz"><i class="fab fa-github"></i></a>

      </p>
    </div>
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
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.min.css");

body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
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
