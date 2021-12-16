<template>
  <div class="home">
    
    <ListDrop5X/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import ListDrop5X from '~/components/Home/ListDrop5X.vue'

export default Vue.extend({
  name: 'Home',
  components: {
    ListDrop5X
  },
  data() {
    return {
      
    }
  }
})
</script>

<style scoped lang="scss">
.home {
  display: grid;
  padding-top:0px;
  width:100%;
  margin:0 auto;
}
</style>