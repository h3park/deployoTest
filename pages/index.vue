<template>
  <Tutorial/>
  <div>카톡 fullscreen</div>
</template>

<script>
export default {
  name: 'IndexPage',
  mounted(){
    documentElement.requestFullscreen();
  },
}
</script>
