<script setup>
import { ref } from 'vue'

// const hello{}

const options = ref([
    {icon:'inbox',title:'Inbox', number:52 , selected:true},
    {icon:'star',title:'Starred', number:12 , selected:false},
    {icon:'schedule',title:'Snoozed', number:0 , selected:false},
    {icon:'send',title:'Sent', number:2 , selected:false},
    {icon:'task',title:'Drafts', number:7 , selected:false},
    {icon:'expand_more',title:'More',selected:false},
])

</script>

<template>
    <div class="options">
        <div class="option" v-for="option in options" :class="{bg:!option.selected}">
            <span class="material-icons">{{option.icon}}</span>
            <h4 :class="{bg:!option.selected}">{{option.title}}</h4>
            <p v-if="option.selected" :class="{bg:!option.selected}">{{option.number}}</p>
        </div>
    </div>
</template>


<style scoped>
    .options{

    }
    .option{
        display:flex;
        align-items:center;
        height: 40px;
        padding: 0 10px;
        border-top-right-radius: 20px;
        border-bottom-right-radius:20px ;
        cursor: pointer;
    }

    .option,
    .option > p,
    .option > h3 {
        background-color:#fcecec;
        color:#c04b37;
        font-weight:800;
    }

    .option span{
        padding:5px
    }
    .option h4{
        flex:1;
        margin-left: 10px;
        font-size: 14px;
    }
    
    .bg{
        background-color:#fff;
        color:#000;
        font-weight:normal;
    }
    .option:hover:not(:first-child){
        background-color: rgba(0, 0, 0,0.1);
    }
    .option:hover h4{
        background-color: transparent
    }
</style>