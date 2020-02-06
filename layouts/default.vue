<template>
  <v-app >
    <v-content>
      <v-container>
        <div class="main">
         <div class="main-bar">
            <v-btn class="ma-2" outlined color="indigo" to="/">HOME</v-btn>
            <v-btn class="ma-2" outlined color="success" to="/login">LOGIN</v-btn>
            <v-btn class="ma-2" outlined color="error" to="/secret">SECRET</v-btn>
         </div>
       </div>
        <nuxt />
      </v-container>
    </v-content>
    
  </v-app>
</template>

<style  scoped>

.main {

margin: 20px;
display: flex;
align-items: center;
justify-content: center;
flex-direction: column;

}

.main-bar {
  width: 30%;

  margin: 10px 20px;
  display: flex;
  justify-content: space-between;
  
}

.html {
  list-style: none;
  text-decoration: none;

}

</style>



