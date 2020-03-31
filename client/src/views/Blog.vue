<template>
  <Layout>
    <HeroBanner>
      <h1>Blogsley Blog</h1>
    </HeroBanner>
    <main class="landing-main">
      <div class="columns is-gapless">
        <div class="column">
          <div class="landing-heading">
            <div class="landing-title">Latest Posts</div>
          </div>
        </div>
        <div class="column is-four-fifths">
          <Articles/>
        </div>
      </div>
    </main>
  </Layout>
</template>

<script>
import HeroBanner from '../components/HeroBanner';

export default {
  components: {
    HeroBanner,
  },
  metaInfo() {
    return {
      title: 'Kurtis Fields',
      meta: [
        { name: 'description', content: 'Web Developer' },
      ],
    };
  },
};
</script>

<style lang="scss">
/*
.landing-main {
  position: relative;
}
*/
.landing-title {
  font-size: 2em;
  white-space: nowrap;
  opacity: .5;
}
@media only screen  and (min-width : 1224px) {
  .landing-title {
    font-size: 3em;
    transform: rotate(-90deg);
    padding-top: 3em;
  }
}

/* Tablet (landscape) ----------- */
@media only screen and (max-width : 1223px) {
  .landing-main {
    // padding-left: 1em;
  }
  .landing-heading {
    //padding-top: 3em;
    padding-right: 3em;
    transform: none;
    text-align: right;

  }
  .landing-title {
    //transform: none;
    transform: rotate(-90deg);
  }
}

/* Smartphones (portrait) ----------- */
@media only screen and (max-width : 800px) {
  .landing-main {
    // padding-left: 1em;
  }
  .landing-heading {
    padding-left: 1em;
    transform: none;
  }
  .landing-title {
    transform: none;
  }
}

</style>
