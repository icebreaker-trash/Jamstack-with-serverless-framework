<template>
  <div class="container">
    <div>
      <Logo />
      <div>Deploy Time: UTC+8 (static)</div>
      <h2>
        <span>server:</span> {{day}}
      </h2>
      <h2> <span>client:</span> {{clientDay}}</h2>

    </div>

  </div>
</template>

<script>
import dayjs from "dayjs";
export default {
  data() {
    return {
      clientDay: dayjs().format("YYYY-MM-DD HH:mm:ss"),
    };
  },
  asyncData() {
    return {
      day: dayjs().format("YYYY-MM-DD HH:mm:ss"),
    };
  },
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
