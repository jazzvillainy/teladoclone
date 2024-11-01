<script>
import Signupform from "./components/Signupform.vue";
import BlockTwo from "./components/BlockTwo.vue";
import Header from "./components/Header.vue";
// import BlockTwo from "./components/BlockTwo.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: { Signupform, BlockTwo, Header, Footer },
};
</script>

<template>
  <div class="outterShell">
    <Header />
    <BlockTwo />
    <Signupform />
    <Footer />
  </div>
</template>

<style>
/* * {
  border: solid;
} */
.outterShell {
  width: 100%;
}
/* body {
  margin: 0;
}
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
.createSectionWrapper5e201 {
  display: flex;
  flex-direction: column;
  align-items: center;
} */
</style>
