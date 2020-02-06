<template>
  <v-container>
    
    <form>
        <v-text-field
        v-model="editedPost.author"
        label="Name"
        required
        ></v-text-field>
        <v-text-field
        v-model="editedPost.title"
        label="title"
        required
        ></v-text-field>
        <v-text-field
        v-model="editedPost.content"
        label="content"
        required
        ></v-text-field>
        <v-btn class="mr-4" @click="submit">submit</v-btn>
        <v-btn >clear</v-btn>
    </form>

  

  </v-container>
</template>

<script>
    export default {
        props: {
            post: {
            type: Object,
            required: false
            }
        },

        data() {
            return {
            editedPost: this.post
                ? { ...this.post }
                : {
                    author: "",
                    title: "",
                    content: ""
                }
            };
        },

    methods:{
        submit(){
           
            this.$emit('clickss',this.editedPost)
            
            this.$router.push("/");
        }
    }


    }
</script>