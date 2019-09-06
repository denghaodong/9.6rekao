<template>
  <div id="app">
    <div class="content">
      <router-view/>
    </div>
    <div class="bottom">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </div>
  </div>
</template>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  list-style-type: none;
}
html,body,#app{
  width: 100%;
  height: 100%;
}
#app{
  display: flex;
  flex-direction: column;
}
.content{
  width: 100%;
  height: 100%;
}
.bottom{
  width: 100%;
  height: 30px;
  background: #ccc;
  display: flex;
  a{
    width: 50%;
    height: 100%;
    text-decoration: none;
    color: #333;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
