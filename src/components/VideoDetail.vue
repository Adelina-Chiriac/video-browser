<template>
  <div class="col-md-8" v-if="video">
    <div class="ratio ratio-16x9">
      <iframe :src="videoUrl" />
    </div>
    <div class="details">
      <h4>{{ video.snippet.title }}</h4>
      <p>{{ video.snippet.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "VideoDetail",
  props: {
    video: Object
  },
  computed: {
    videoUrl: function() {
      const videoId = this.video.id.videoId;
      
      return `https://www.youtube.com/embed/${videoId}`;
    }
  }
}
</script>

<style scoped>
  .details {
    margin-top: 10px;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
  }
</style>