<template>
  <header>
    <h1>{{ valor }}</h1>
  </header>
</template>

<script>
export default {
  props: ["valor"],
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald&family=Poppins:wght@100;200&family=Raleway:ital,wght@0,200;0,300;1,200&family=Roboto+Condensed:ital,wght@0,300;1,300&display=swap');
header {
  background-color: rgb(173, 68, 68);
  color: white;
  height: 60px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Raleway', sans-serif;
}
</style>