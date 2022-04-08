<template>
<div class ="week" v-for="week in weeks" :key="week">
    <router-link :to="{name : 'Week' , params: {id: week}}">
        <h2>week-{{week}}</h2>
    </router-link>
</div>
</template>

<script>
import Week from './Week.vue'
export default {
    name: 'Quiz',
    components:{
        Week,
    },
    data(){
        return{
            weeks : 12
        }
    }

}
</script>

<style Scope>
.week{
    background: #f4f4f4;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 600px;
    cursor: pointer;
    color: #444;
}
.week h2:hover{
    background: #ddd;
}
.week a{
    text-decoration: none;
}

</style>