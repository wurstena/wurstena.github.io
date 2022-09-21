<template>
<div class="wrapper">
  <div class="photos">
    <div class="photo" v-for="photo in photos" :key="photo.id">
      <!--div :id="'picture' + photo.id" v-on:click="showInfo()">
        <img :src="'/images/'+photo.image">
      </div-->
      <div class="picture" v-if="photo.info">
        <img :src="'/images/' + photo.image" v-on:click="showInfo(photo)">
      </div>
      <div class="info" v-else>
        <div class="container" v-on:click="hideInfo(photo)">
          <h5>{{photo.name}}</h5>
          <h6>Date: {{photo.date}}</h6>
          <h6>Location: {{photo.location}}</h6>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'PhotoList',
  props: {
    photos: Array,
  },
  methods: {
    showInfo(photo) {
      photo.info = false;
    },
    hideInfo(photo) {
      photo.info = true;
    }
  }
}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.photos {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.photo {
  margin: 10px;
  margin-top: 50px;
  width: 300px;
}

.photo img {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 20px;
  align-items: center;
  margin-bottom: 5px;
  background-color: #f5c1c1;
  border-radius: 10px;
  color: #393939;
}

.info:hover {
  cursor: pointer;
}

.picture {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 5px;
}

.picture:hover {
  cursor: pointer;
}

.auto {
  margin-left: auto;
}
</style>
