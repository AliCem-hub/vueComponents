<template>
  <div class="info" :class="Style">
    <div class="info-icon" v-if="Icon">
      <img alt="info-img" :src="getImgUrl(pic)" style="width: 35px;">

    </div>

    <div class="info-content">
       <h1 class="info-header" v-if="Header">{{ Header }}</h1>
      <h3 class="info-text" v-if="Text">{{ Text }}<button class="btn btn-success">{{ ButonAciklama }}</button>
</h3>

    </div>
  </div>
</template>

<script>

export default {
  props: [
    'Header',
    'Text',
    'ButonAciklama',
    'Style',
    'Border',
    'FontType',
    'Icon'
  ],
  methods:{
    getImgUrl() {
    var images = require.context('../assets/', false, /\.png$/)
    return images('./' + this.Icon + ".png")
    }
  }
}
</script>

<style scoped>
.info {
  width: 45%;
  padding-top: 9px;
  padding-bottom: 80px;
  padding-left: 20px;
  margin-left: 500px ;
  border-radius: 80px;
  margin-top: 100px;

}
.info-icon {
  width: 10%;
}
.info-content {
  width: 80%;
}
.info-content .info-header {
  color:red;
    margin-left: 80px ;
}
.info-content .info-text {
  color:black;
  margin-left: 80px ;
}
.info-content .btn-success {
  color: rgb(232, 237, 229);
}
.info.blue-info {
  background: lightskyblue;
  border: black;
  color: blue;
}
.info.green-info {
  background: palegreen;
  border: black;
  color: green;
}
.info.yellow-info {
  background: rgb(199, 199, 92);
  border: black;
  color: black;
}
.info.red-info {
  background: rgb(224, 107, 107);
  border: black;
  color: red;
}
</style>