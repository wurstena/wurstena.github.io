<template>
<div id="app">
  <div class="header">
    <img class="logo" src="public/images/Wedding-Logo.png">
  </div>

  <div class="navbar-container">
    <nav class="navbar navbar-expand-lg navbar-light bg-light sticky-top">
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-center" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <router-link to="/">
            <div class="menu-item home">
              <p>Home</p>
            </div>
          </router-link>
          <router-link to="/photos">
            <div class="menu-item photos">
              <p>Photos</p>
            </div>
          </router-link>
          <router-link to="/registry">
            <div class="menu-item registry">
              <p>Registry</p>
            </div>
          </router-link>
          <router-link to="/virtual">
            <div class="menu-item virtual">
              <p>Virtual Attendance Information</p>
            </div>
          </router-link>
          <router-link to="/rsvp">
            <div class="menu-item rsvp">
              <p>RSVP</p>
            </div>
          </router-link>
          <router-link to="/map">
            <div class="menu-item map">
              <p>Utah Reception Map</p>
            </div>
          </router-link>
        </div>
      </div>
    </nav>
  </div>
  <router-view />

  <nav class="navbar sticky-bottom navbar-light bg-light footer">
    <span class="navbar-text">
      Find me on <a href="https://github.com/wurstena" target="_blank">GitHub</a>
    </span>
  </nav>
</div>
</template>

<script>
export default {
  computed: {
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Times New Roman", serif;
  text-decoration: none;
}

img {
  width: 100%;
  height: 100%;
}

.page {
  display: flex;
  flex-wrap: wrap;
  overflow: hidden;
  flex-direction: column;
  background-color: #E9E9E9;
}

.header {
  display: flex;
  flex-wrap: wrap;
  background-color: #33445c;
  justify-content: center;
}

.logo {
  justify-content: center;
  width: 50%;
}

.navbar {
  background-color: #c5c5c5 !important;
  color: white;
  text-decoration: none;
}

.navbar-nav {
  display: flex;
  justify-content: space-between;
}

.menu-item {
  font-size: 1.1em;
  color: #393939;
  text-decoration: none;
  padding-left: 1.5em;
  padding-right: 1.5em;
  padding-top: 5px;
  font-family: "Times New Roman", serif;
}

.menu-item:hover {
  color: gray;
  text-decoration: none;
}

router-link {
  text-decoration: none;
}

.footer {
  justify-content: center;
}

.image-row {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
.image-row img {
  margin: 10px;
  box-shadow: 3px 3px 8px 0px rgba(0,0,0,0.3);
  max-width: 25vw;
}



/* Timeline */
.timeline-container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: center;
  width: 75%;
  margin-top: 50px;
  margin-left: 12.5%;
  margin-right: 12.5%;
  margin-bottom: 50px;
  background-color: #d9d9d9;
  padding-top: 20px;
  padding-bottom: 20px
}
.timeline-container h1 {
  font-family: "Times New Roman", serif;
  text-align: center;
}
.timeline-container h5, p {
  font-family: "Times New Roman", serif;
}

.circle {
  padding: 13px 20px;
  border-radius: 50%;
  background-color: #ED8D8D;
  color: #fff;
  max-height: 50px;
  z-index: 2;
}

.timeline-section.row .col-2 {
  align-self: stretch;
}
.timeline-section.row .col-2::after {
  content: "";
  position: absolute;
  border-left: 3px solid #ED8D8D;
  z-index: 1;
}
.timeline-section.row .col-2.bottom::after {
  height: 50%;
  left: 50%;
  top: 50%;
}
.timeline-section.row .col-2.full-left::after {
  height: 100%;
  left: 50%;
}
.timeline-section.row .col-2.full-right::after {
  height: 100%;
  right: 50%;
}
.timeline-section.row .col-2.top::after {
  height: 50%;
  right: 50%;
  top: 0;
}
.timeline div {
  padding: 0;
  height: 40px;
}
.timeline hr {
  border-top: 3px solid #ED8D8D;
  margin: 0;
  top: 17px;
  position: relative;
}
.timeline .col-2 {
  display: flex;
  overflow: hidden;
}
.timeline .corner {
  border: 3px solid #ED8D8D;
  width: 100%;
  position: relative;
  border-radius: 15px;
}
.timeline .top-right {
  left: 50%;
  top: -50%;
}
.timeline .left-bottom {
  left: -50%;
  top: calc(50% - 3px);
}
.timeline .top-left {
  left: -50%;
  top: -50%;
}
.timeline .right-bottom {
  left: 50%;
  top: calc(50% - 3px);
}


/* Secondary Page Content */
.page-body {
  padding-top: 15px;
  padding-bottom: 15px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  flex-direction: column;
  align-items: center;
}
.page-body h1 {
  padding-top: 10px;
}
.page-body h1, p {
  font-family: "Times New Roman", serif;
  text-align: center;
}
.content-container {
  margin-top: 30px;
  width: 75%;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  flex-direction: column;
  background-color: #d9d9d9;

  margin-bottom: 50px;
  padding-top: 20px;
  padding-left: 20px;
  padding-right: 20px;
  padding-bottom: 30px;

  border-radius: 10px;
}
.content-text {
  width: 75%;
  text-align: center;
}
.button-container {
  display: flex;
}
.button-external {
  margin-bottom: 20px;
  margin-right: 20px;
  margin-left: 20px;
  border-radius: 10px;
  padding: 10px;
  background-color: #fab4b4;
  color: black;
}
.button-external:hover {
  color: black;
  text-decoration: none;
  background-color: #ED8D8D;
}




/* photos page grid */
.row {
  display: flex;
  flex-wrap: wrap;
  padding: 0 4px;
}

/* Create four equal columns that sits next to each other */
.column {
  flex: 33%;
  max-width: 33%;
  padding: 0 4px;
}

.column img {
  margin-top: 8px;
  vertical-align: middle;
  width: 100%;
  height: auto;
}

.column img:last-child {
  margin-bottom: 8px;
}


/* Responsive layout - makes a two column-layout instead of four columns */
@media screen and (max-width: 800px) {
  .image-row {
    flex-direction: column;
  }
  .image-row img {
    max-width: 50vw;
  }

  .column {
    flex: 50%;
    max-width: 50%;
  }
  .logo {
    width: 75%;
  }
}

/* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .image-row {
    flex-direction: column;
  }
  .image-row img {
    max-width: 90vw;
  }

  .column {
    flex: 100%;
    max-width: 100%;
  }
  .logo {
    width: 75%;
  }

  .button-container {
    flex-direction: column;
    justify-content: space-between;
    align-items: space-between;
  }
}


</style>
