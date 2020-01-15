<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/">SimaCatalunya</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Inici</g-link>
        <g-link class="nav__link" to="/about">Qui som?</g-link>
        <g-link class="nav__link" to="/preguntes">Preguntes freqüents</g-link>
      </nav>
    </header>
    <transition name="component-fade" appear>
      <div>
        <slot/>
      </div>      
    </transition>
  </div>
</template>

<static-query>
query {
  metaData {
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

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}


.component-fade-enter-active, .component-fade-leave-active {
  transition: opacity 1s ease;
}
.component-fade-enter, .component-fade-leave-to
/* .component-fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
