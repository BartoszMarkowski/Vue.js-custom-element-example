<template>
  <div>
    <button v-on:click="increase">click</button>
    <div>{{ i }}</div>
  </div>
</template>
<script>
  export default {
    props: ['when'], 
    data: function () {
      return {
        i: 0
      }
    },
    methods: {
      increase: function () {
        this.i++;
        if(this.i == this.when) {
           this.$emit('equal', this.i);
        }
      }
    }
  }
</script>