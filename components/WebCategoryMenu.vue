<template>
<div>
    <div class="pt-10" :style="{ fontSize:'18px', fontWeight:'600'}">카테고리에서 인기있어요!</div>
      <div class="ml-n16" :style="{ position:'relative',zIndex:'100', width:'100%'}">
            <v-sheet
                
                elevation="0"
                width="1270px"
            >
                <v-slide-group
                v-model="model"
                class="py-4"
                active-class="success"
                
                >
                <v-slide-item
                    v-for="n in 15"
                    :key="n"
                    v-slot="{ active, }"
                >
                    <v-card
                    :color="active ? undefined : 'lighten-1'"
                    class="ma-4"
                    height="150"
                    width="222"
                    
                    
                    >
                      <v-skeleton-loader
                        v-bind="attrs"
                        type="article"
                        ></v-skeleton-loader>
                    <v-row
                        class="fill-height"
                        align="center"
                        justify="center"
                    >
                        <v-scale-transition>
                        <v-icon
                            v-if="active"
                            color="white"
                            size="48"
                            v-text="'mdi-close-circle-outline'"
                        ></v-icon>
                        </v-scale-transition>
                    </v-row>
                    </v-card>
                </v-slide-item>
                </v-slide-group>
            </v-sheet>
          
          
      </div>
    </div>  
</template>

<script>
export default {
    data() {
    return {
      name: "Nuxt.js",
      model: null,

      randomimg: [],
      attrs: {
        class: "",
        boilerplate: true,
        elevation: 0,
      },
    };
  },

}
</script>

<style>

</style>