<template>
  <div class="preview">
    <router-link :to="`/projects/${article.slug}`" >
      <div class="previewImage">
        <g-image :alt="article.title" :src="article.cover"/>
      </div>
      <div class="previewTitle">
        {{article.title}}
      </div>
      <p>
        {{article.description}}
      <p/>
    </router-link>
    <!-- <div class="previewDate">
      <small class="previewDate">{{article.date}}</small>
    </div> -->
  </div>
</template>
<script>
export default {
  name: 'ArticlePreview',
  props: ['article'],
  components: {
  },
  data () {
    return {
    }
  }
}
</script>
<style  lang="scss">
.preview {
  padding-bottom: 1rem;
}
.previewTitle {
  font-size: 1.5rem;
  margin-top: .5rem;
  margin-bottom: .5rem;
  // line-height: 1rem;
}
.previewImage {
  max-height: 200px;
  overflow: hidden;
  height: 100%;
  width: 100%;
  object-fit: cover;
}

.previewDate {
  text-align: right;
}

.tag {
  color: #A0A0A0;
  text-decoration: none;
  display: inline-block;
  padding: .33333rem .5rem;
  line-height: 1;
  border-radius: 2px;
  border: 1px solid #A0A0A0;
  margin-right: .5em;
}
</style>