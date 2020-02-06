<template>
    <div class="itemList">
        
            <v-card
            class="mx-auto"
            max-width="400"
            
            >
                <v-card-title v-text="title" ></v-card-title>
                <v-card-subtitle v-text="author" ></v-card-subtitle>
                <v-card-text v-text="content" ></v-card-text>
                <v-card-actions>
                    <v-btn
                        text
                        color="deep-purple accent-4"
                        :href="postLink"
                    >
                        More
                    </v-btn>
                </v-card-actions>
                

            </v-card>

      
    </div>
</template>

<script>
export default {
    
    
    data: () =>({
    
    }),
    props: {
    id: {
      type: String,
      required: true
    },
    isAdmin: {
      type: Boolean,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    author: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    }
  },
  computed:{
      postLink(id){
          return this.isAdmin ? '/secret/' + this.id : '/posts/' + this.id
      }
  }

}
  

</script>