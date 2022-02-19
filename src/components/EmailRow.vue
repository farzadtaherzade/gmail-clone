<script setup>
    import { ref } from 'vue';

    const icons = ref([
        'check_box_outline_blank',
        'star',
        'label'
    ])

    const options = ref([
        {title:'Test', subject:'Best subject', desc:'This is desc', time:'16 Feb'},
        {title:'HTML', subject:'html code nevisi', desc:'Html not a programing lang ', time:'16 Feb'},
        {title:'CSS', subject:'styleshee', desc:'We using css for get style a web page', time:'16 Feb'}
    ])
</script>

<template>
    <div class="email-row" v-for="option in options">
        <div class="icons">
            <span class="material-icons">{{icons[0]}}</span>
            <span class="material-icons">{{icons[1]}}</span>
            <span class="material-icons">{{icons[2]}}</span>
        </div>

        <div class="flex">
            <h3 class="title">{{option.title}}</h3>

            <div class="message">
                <h4>{{option.subject}} <span class="message-desc">- {{option.desc}} </span> </h4>
            </div>
        </div>

        <span class="time">
            {{option.time}}
        </span>

    </div>
</template>

<style scoped>
    .email-row{
        display: flex;
        align-items: center;
        flex-wrap: no-wrap;
        height:50px;
        border-bottom:1px solid whitesmoke;
        border-top: 1px solid whitesmoke;
        cursor: pointer;
        z-index: 999;
    }
    .email-row:hover {
        box-shadow: 0px 4px 4px -2px rgba(0,0,0,0.24);
    }
    .icons span {
        font-size: 18px;
        padding-right: 10px;
        color: rgba(0,0,0,0.2);
    }
    .icons{
        display: flex;
        align-items: center;
    }
    .message{
        display: flex;
        align-items: center;
        flex: .8;
        font-size: 14px;
    }
    .message h4 {
        width: 400px;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
        padding-left: 5px;
        padding-right: 5px;
    }
    .title{
        margin-left: 2px;
        font-size:14px;
        flex:.1;
    }
    .time{
        padding-right:15px;
        font-size:9px;
        font-weight:bold;
    }
    .message-desc{
        font-weight: 400;
        color: gray;
    }
    .flex {
        display: flex;
        flex: 1;
    }

    @media (max-width: 560px) {
        .material-icons:not(:first-child , :last-child) {
            display: none;
        }
        .flex{
            flex-direction: column;
        }
    }
    @media (max-width: 320px) , (max-width:425px) {
        .material-icons:not(:first-child) {
            display: none;
        }
        .message h4 {
            display: inline;
        }
        .flex{
            flex-direction: column;
        }
    }
    
</style>
