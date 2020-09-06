<!--
 * @Author: your name
 * @Date: 2020-09-06 01:10:04
 * @LastEditTime: 2020-09-06 03:56:46
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /reveille-recruiterz/src/views/Settings.vue
-->
<template>
    <h1>Setting</h1>
    <div>
        <ul class = "nav navbar-nav">
            <li><router-link to = "/">Home</router-link></li>
            <li><router-link to = "/">MyProfile</router-link></li>
            <li><a href="#" @click.prevent="logout">Logout</a></li>
        </ul>
    </div>

</template>

<!-- comment contents here -->
<script>
// import MyProfile from './MyProfile.vue'
import HomePage from './HomePage.vue'

export default {
    data: () => ({
            csrf: document.querySelector('meta[name="csrf-token"]').getAttribute('content'),
            }),   
    methods:{
        logout:function(){
            axios.post('logout').then(response => {
                if (response.status === 302 || 401) {
                console.log('logout')
                }
                else {
                // throw error and go to catch block
                }
            }).catch(error => {

            });
        },
    },
}
</script>


<style lang = "stylus" scoped>
#app {
    max-width: 400px;
    margin: 0 auto;
    line-height: 1.4;
}
h1 {
    text-align: center;
}
p {
    font-size: 1em;
    text-align: center;
}

</style>