<template>
  <div id="header-container" class="sticky-top">
    <b-container
      fluid
      id="header"
      class="text-light d-flex justify-content-center align-items-center "
    >
      <div>
        <p class="text-shadow display-3">Hi, I'm</p>
        <p class="text-shadow display-1">Garrett Hensley</p>
        <p class="text-shadow display-4 d-none d-sm-block">Web Developer</p>
        <p class="text-shadow lead d-block d-sm-none">Web Developer</p>
      </div>
    </b-container>
  </div>
</template>

<style scoped>
.text-shadow {
  text-shadow: 0.05em 0.05em 0.05em rgba(0, 0, 0, 0.8);
  margin: 0;
}
#header-container {
  z-index: -1 !important;
}
#header {
  height: 100vh;

  -webkit-animation: fadein 2s; /* Safari, Chrome and Opera > 12.1 */
  -moz-animation: fadein 2s; /* Firefox < 16 */
  -ms-animation: fadein 2s; /* Internet Explorer */
  -o-animation: fadein 2s; /* Opera < 12.1 */
  animation: fadein 2s;
}

.lead {
  font-size: 3em;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/* Animations B) */
/* Firefox < 16 */
@-moz-keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Safari, Chrome and Opera > 12.1 */
@-webkit-keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Internet Explorer */
@-ms-keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Opera < 12.1 */
@-o-keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
