<template>
  <div class="fact-card">
    <h3>{{ fact }}</h3>
  </div>
</template>

<script>
export default {
  props: {
    fact: String,
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Leckerli+One&family=Roboto+Slab&family=Source+Code+Pro&display=swap");
.fact-card {
  margin-left: 25%;
  margin-right: 25%;
  padding: 17px;
  margin-bottom: 24px;
  margin-top: 5%;
  transition: all 0.2s linear;
  cursor: pointer;
  border-radius: 15%;
  background-color: rgb(43, 38, 97);
  width: 50%;
}
.fact-title {
  font-family: "Roboto Slab", serif;
  font-size: 20px;
  color: #2c3e50;
}

.fact-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2), 0 1px 15px 0 rgba(0, 0, 0, 0.19);
}
.fact-card > .fact-title {
  margin: 0;
}

.fact-link {
  color: black;
  text-decoration: none;
  font-weight: 100;
}

.img {
  border-radius: 60%;
  padding: 15px;
}
</style>
