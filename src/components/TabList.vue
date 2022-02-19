<script setup>
    import { ref } from 'vue';

    const options = ref([
        {icon:'inbox', title:'Primary', class:'red' , selected: true},
        {icon:'people', title:'Social', class:'blue' , selected: false},
        {icon:'local_offer', title:'Promotions', class:'green' , selected: false},
    ])

    function changeColor(e) {
        if (e.icon === 'inbox') {
            options.value[0].selected = true
            options.value[1].selected = false
            options.value[2].selected = false
        }else if (e.icon === 'people') {
            options.value[0].selected = false
            options.value[1].selected = true
            options.value[2].selected = false
        }else if (e.icon === 'local_offer') {
            options.value[0].selected = false
            options.value[1].selected = false
            options.value[2].selected = true
        }
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
        min-width: 250px;
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
    .tab-list span {
        font-size: 19px;
    }
    .tab-list:hover{
        background-color: rgba(0, 0, 0,.05);
    }
    .tab-list:hover:not(:first-child){
        background-color: rgba(0, 0, 0,.05);
        color: #000;
    }

    @media (max-width: 560px) {
        .tab-list {
            display: none;
        }
    }

</style>