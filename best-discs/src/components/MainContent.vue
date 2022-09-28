<template>
    <section class="container-discs">
         <div class="discs">
            <div class="disc" v-for="item in albums" :key="item.poster">
             <img :src="item.poster" alt="">
             <p>{{ item.title }}</p>
            </div>
          
         </div>
    </section>
</template>

<script>

import axios from 'axios'
export default {
name: 'MainContent',
data(){
    return{
        albums:[],
        
    }
},

created(){
  axios.get('https://flynn.boolean.careers/exercises/api/array/music')
       .then((response) => {
        if (response.status === 200) {
          console.log('ok')
          const albumsAPI = response.data.response
          this.albums = albumsAPI
          console.log(this.albums)
        }
                        })},
}

</script>

<style scoped>

.discs{
        width: 1200px;
        margin: 0 auto;
        display: flex;
        align-items: center;
        flex-wrap: wrap;
        padding-top:150px ;
    }
.container-discs{
    background-color: hsl(209deg 33% 17%);
    height: 907px;
}
.disc{
    width: calc(90% / 5);
    height: 350px;
    background-color: hsl(210deg 21% 23%);
    margin: 10px 10px;
}
img{
    width: 184px;
    height: 184px;
    margin-left: 16px;
    margin-right: 16px;
    margin-top: 10px;
}
</style>

