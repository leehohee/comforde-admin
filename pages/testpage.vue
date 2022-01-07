<template>
    <div width="100%" class="grey text-center hohee">
        <v-form @submit.prevent="onSubmitForm">
            <h4>누구를?</h4>
            <v-text-field
            class="white"
            v-model="bomis"
            outlined
            >

            </v-text-field>
            <v-btn x-large type="submit"><h4>가랏!</h4></v-btn>
        </v-form>
        <v-list-item v-for="(bomi,i) in cutebomi" :key="i" dense>
            
            
            <h1>{{bomi}}</h1>
            
        </v-list-item>
    </div>
</template>

<script>
export default {
    data(){
        return {
            bomis:'',
            cutebomi:[],
        } 

        
    },
    methods:{
        onSubmitForm(){


            
            this.cutebomi.push(this.bomis);

        }
            
        
    }
}
</script>

<style scope>
.hohee {
    color: blue;
    font-size:60px;
    height: 500px;
}
</style>