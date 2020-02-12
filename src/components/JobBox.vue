<template>
    <div class="job" v-bind:class="{fullh:fullh}" @click="open">
        <div class="job-header">
            <p class="job-title"> {{ jt }} </p>
            <div class="open" v-bind:class="{ rotate: rotate }">»</div>
        </div>
        <div class="job-des">
          {{ jd }}
        </div>
    </div>
</template>
<style>
.job{
    transition: all 3s ease-in-out;
    width: 100%;
    height: 76px;
    border-radius: 24px;
    margin-top: 28px;
    padding: 16px;
    background-color: #E8E8E8;
    box-shadow: 2px 6px 16px rgba(135,135,135,0.15), -4px -2px 16px rgba(255,255,255,.65);
    overflow: hidden;
}
.fullh{
  height: auto !important;
}
.job-header{
    height: 44px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.job-title{
    font-weight: bold;
}
.open{
    width: 44px;
    height: 44px;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    transform: rotate(90deg);
}
.rotate{
    align-items: flex-end !important;
    transform: rotate(-90deg) !important;
}
.job-des{
    margin-top: 16px;
    height: 100%;
}
</style>

<script>
export default {
  name: "JobBox",
  data() {
    return{
      rotate: false,
      fullh: false
    }
  },
  props: {
    jt: String,
    jd: String
  },
  methods: {
    open(){
      this.rotate = !this.rotate;
      this.fullh = !this.fullh;
    }
  }
};
</script>