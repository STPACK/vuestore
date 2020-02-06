<template>
  <v-container>
    <div class="head">
      <h2>Home page</h2>
      <v-btn class="ma-2" outlined color="indigo" to="/add">new item</v-btn>

    </div>

    <div>
        <itemList
        :posts ="loadedPost"
        
        />

    </div>
  </v-container>
</template>

<script>
import itemList from '@/components/itemList'

export default {
  components:{
    itemList
  },
  computed:{
    loadedPost(){
      return this.$store.getters.loadedPosts
    }
  }


}
</script>

<style scoped>

.head{
display: flex;
align-items: center;
justify-content: center;
flex-direction: column;

}
</style>