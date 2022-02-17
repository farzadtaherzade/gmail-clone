<script setup>
    import { ref } from 'vue';

    const options = ref([
        {icon:'inbox', title:'Primary', class:'red' , selected: true},
        {icon:'people', title:'Social', class:'blue' , selected: false},
        {icon:'local_offer', title:'Promotions', class:'green' , selected: false},
    ])

    function changeColor(e) {
        console.log(e)
    }
</script>

<template>
    <div class="tab-list" v-for="option in options" :class="[ option.selected ? option.class :'']" @click="changeColor(option)">
        <span class="material-icons">{{option.icon}}</span>
        <h4>{{option.title}}</h4>
    </div>  
</template>



<style scoped>
    .tab-list{
        display: flex;
        align-items: center;
        border-bottom-width:2px ;
        padding: 18px 20px;
        margin-top:9px;
        min-width: 200px;
        cursor: pointer;
        color: gray;
    }
    .tab-list h4 {
        font-size: 14px;
        margin-left: 15px;
    }
    .red{
        border-bottom: 3px solid red;
        color: red;
        background-color: #fff;
        border-width: 3px;
    }
    .blue{
        border-bottom: 3px solid blue;
        color: blue;
        background-color: #fff;
        border-width: 3px;
    }
    .green{
        border-bottom: 3px solid green;
        color: green;
        background-color: #fff;
        border-width: 3px;
    }
</style>