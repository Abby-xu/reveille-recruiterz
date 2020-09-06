<!--
 * @Author: Rong
 * @Date: 2020-09-06 01:10:04
 * @LastEditTime: 2020-09-06 06:37:14
 * @LastEditors: Please set LastEditors
 * @Description: 
 1. Check the website for dubbuging: https://vuetifyjs.com/zh-Hans/components/cards/
 2. make sure the link of Login and Dashboard are useful
 3. Check the color, I assigned color randomly...<template>
 4. Check the Text in the box, I think it probably needs to be more specific
 </template>
 * @FilePath: /reveille-recruiterz/src/views/HomePage.vue
-->
<template>
    <!-- using el-container -->
    <el-container>
        <!--- header --->
        <el-header height = "60px">
            <li><router-link to = "/">Log in</router-link></li>
        </el-header>
        
        <!-- real Header -->
        <h1>Reveille Recruiter</h1>


        <div class="text-center">
            <v-btn rounded color="primary" dark>
                <li><router-link to = "/">Dash Board</router-link></li>
                    <!------------ Dashboard page, need to add the link ------------>
            </v-btn>
        </div>

        <v-divider></v-divider>

        <el-row>
            <el-col :span="8"><div class="grid-content"></div>
                Fair
            </el-col>
            <el-col :span="8"><div class="grid-content"></div>
                Safe
            </el-col>
            <el-col :span="8"><div class="grid-content"></div>
                Institute
            </el-col>
        </el-row>

        <el-footer heaight = "30px">&copy;HowdyHack 2020</el-footer>
    </el-container>

</template>

<script>
// import MyProfile from './MyProfile.vue'
import HomePage from './HomePage.vue'

// need to implement
</script>


<style lang = "stylus" scoped>



.el-header {
  background-color: #409EFF;
  color: white;
}
.el-footer {
  background-color: #909399;
  color: black;
  text-align: center;
}
.grid-content {
    background-color: thistle;
}

h1 {
    text-align: center;
}

</style>