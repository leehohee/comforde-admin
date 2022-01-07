<template>
    <v-app>
            

            <v-app-bar
            class="white"
            app
            dense
            flat
            outlined
            justify="space-between"
            no-gutter
            
            >
                
                    
                    
                    <v-spacer></v-spacer>
                    
                    <v-toolbar-title>
                        
                        <nuxt-link to="/"><h4>관리자페이지</h4></nuxt-link>
                        
                    </v-toolbar-title>
                    
                    <v-spacer></v-spacer>
                    
                    <v-btn icon :style="{ marginRight:'0px',paddingRight:'0px',display:'flex', alignItems: 'center'}">
                            <v-icon>mdi-magnify</v-icon>
                    </v-btn>
                    
                    
                
            </v-app-bar>
            
            <v-navigation-drawer
            v-model="drawer"
            app
            :style="{zIndex:'100',}"
            hide-overlay
            width="200"
            clipped
            
            >

                <v-list-item>
                    <v-list-item-avatar>
                    <v-img :src="require('@/assets/iconimg.png')" />
                    </v-list-item-avatar>
                    <v-list-item-content>
                    <v-list-item-title class="text-h6">
                        COMFORDE
                    </v-list-item-title>
                    <v-list-item-subtitle>
                        메뉴
                    </v-list-item-subtitle>
                    </v-list-item-content>
                </v-list-item>
                
                <v-row>
                    <v-col>
                        <v-container>
                           
                            <v-list-item
                            v-for="(item,i) in items"
                            :key="i"
                            dense
                            >
                                <!-- <v-list-item-icon>
                                    <v-icon v-text="i+1"></v-icon>
                                </v-list-item-icon> -->
                                <v-list-item-content>
                                    <v-list-item-title><nuxt-link :to="`/${item.src}`">{{item.name}}</nuxt-link></v-list-item-title>
                                </v-list-item-content>
                            </v-list-item>
                        </v-container>
                        

                    </v-col>
                </v-row>
            </v-navigation-drawer>
            
            <v-main>
            <v-col cols="12" md="12">





            <nuxt />






            </v-col>
            
            </v-main>


                
            <v-footer app>
            
            </v-footer>    
    </v-app>  
</template>

<script>


export default {
    components: {
        
        
    },
    
    data(){
        return {
            hashtag: '',
            drawer: true,
            items:[
                {
                name: "회원관리",
                src:"manageuser",
                },
                {
                name: "상품관리",
                src:"manageitem",
                },
                {
                name: "결제관리",
                src:"",
                },
                {
                name: "카테고리관리",
                src:"managecategory",
                },
                {
                name: "관리자등록",
                src:"signup",
                },
                
                
                
            ]    
        };
    },
    
    
    methods:{
        onSerachHashtag(){
            this.$router.push({
                path: `/hashtag/${encodeURIComponent(this.hashtag)}`,
            });
            this.hashtag='';
        },
    },

    
}

</script>
    

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@500&display=swap');


    a {
        display:inline-block;
        text-decoration: none;
        color: inherit;
    }
    ul {
        text-decoration: none;
        list-style: none;
    }
    li {
        text-decoration: none;
    }
    h4 {
        font-family: 'Noto Sans KR';
        font-weight: 500;
    }
    


   
</style>