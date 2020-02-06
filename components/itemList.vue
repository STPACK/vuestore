<template>
    <div class="itemList">
        
       <itemPreview
        v-for="post in posts"
        :key="post.id"
        :id="post.id"
        :is-admin="isAdmin"
        :author="post.author"
        :title="post.title"
        :content="post.content"
       
       />
           

   
    </div>
</template>



<script>
import itemPreview from '@/components/itemPreview'
export default {
    components:{
        itemPreview
    },
     props: {
    isAdmin: {
      type: Boolean,
      default: false
    },
    posts: {
      type: Array,
      required: true
    }
  }
    
    
   

}
  

</script>