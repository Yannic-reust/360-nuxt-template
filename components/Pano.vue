<template>
  <div id="coucou" class="panorama-viewer"></div>
</template>

<script lang="ts">
    import * as PANOLENS from "panolens";
export default {
  name: "opening-Hours",

  data() {
    return {};
  },
  methods: {},

  mounted() {
    const panorama = new PANOLENS.ImagePanorama(
      "https://melodious-cranachan-68635f.netlify.app/test/angra.jpg"
    );

    const viewer = new PANOLENS.Viewer({
      container: document.querySelector("#coucou"),
    });

    viewer.add(panorama);
  },
};
</script>

<style>
#coucou{
    height:600px;
}
</style>
