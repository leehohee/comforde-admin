<template>
    <v-container class="ma-0 pa-0" fluid>
    
        
        
        <LoginForm />


        
    </v-container>      
</template>

<script>

import LoginForm from '~/components/LoginForm';

export default {
    components: {
        
        LoginForm,
        
    },
    computed:{
        height (){
            switch (this.$vuetify.breakpoint.name){
                case 'xs' : return 100
                case 'md' : return 500
                default : return 300
            }
        },
        
    },
    data () {
      return {
        
      }
    },
}
</script>

<style>
a {
    text-decoration: none !important;
    color:black !important;
}
.border-top-solid {
    border-top : solid #e6e6e6 1px !important;
}
.border-bottom-solid {
    border-bottom : solid #e6e6e6 1px !important;
}
</style>