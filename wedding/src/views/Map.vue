<template lang="html">
  <div class="wrapper">
    <h2>Utah Reception Location</h2>
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1654.4194911794627!2d-111.90903368965445!3d40.9765656639214!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8752fedec5e6bd2f%3A0x865c612e470ca65!2sLegacy%20Events%20Center%20Building%20%233!5e0!3m2!1sen!2sus!4v1604703643433!5m2!1sen!2sus" width="600" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="css" scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  margin-top: 40px;
  margin-bottom: 100px;
}
h2 {
  margin-bottom: 40px;
  padding-left: 15px;
  padding-right: 15px;
  text-align: center;
}

@media screen and (max-width: 600px) {
  iframe {
    width: 100%;
    padding: 20px;
  }
}
</style>
