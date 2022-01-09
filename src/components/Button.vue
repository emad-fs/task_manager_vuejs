<template>
    <button class="btn" :style="{background:color}" @click="onClick()">{{title}}</button>
</template>


<script>
export default {
  name: "Button",
  props: {
    title: String,
    color: String,
  },
  methods:{
      onClick(){
          console.log('clicked')
      }
  }
};
</script>