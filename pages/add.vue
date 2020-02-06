<template>
  <v-container>
    <h2>New item</h2>  
    <newItem @clickss="onSubmited" />
    

  </v-container>
</template>

<script>
import newItem from '@/components/newItem'
import axios from 'axios'
export default {
    components:{
        newItem
    },
    methods:{
        onSubmited(postdata){
            axios.post('https://nuxt-stp.firebaseio.com/content.json',postdata)
            .then(result => console.log(result))
            .catch(e => console.log(e))
        }
    }
  
  

}
</script>