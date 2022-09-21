<template>
<div>
  <div class="wrapper">
    <h1>Click on a photo for more information!</h1>
  </div>
  <PhotoList :photos="photos" />
</div>
</template>


<script>
import PhotoList from "../components/PhotoList.vue"
export default {
  name: 'Home',
  components: {
    PhotoList
  },
  computed: {
    photos() {
      return this.$root.$data.photos;
    }
  },
}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.wrapper h1 {
  margin-top: 1.5em;
}

h1 {
  text-align: center;
}
</style>
