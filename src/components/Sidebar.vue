<script setup>
import options from './SideBarOptions.vue'
</script>

<template>
    <div class="sidebars">
        <button class="btn">
            <span class="material-icons">add</span>
            Compose
        </button>
        <options />
    </div>
</template>



<style scoped>
    .sidebars {
        flex:.25;
        max-width: 300px;
        padding-right: 20px;
    }
    .btn{
        display:flex;
        align-items: center;

        padding: 15px 30px;
        margin-top: 15px;
        margin-left: 10px;
        margin-bottom: 15px;

        border: none;
        border-radius: 30px;
        background-color: #fff;
        color: gray;
        box-shadow: 0px 2px 5px -2px rgba(0,0,0,.75);
    }

    .btn span{
        margin-right: 10px;
        margin-left: -10px;
    }
    .material-icons:hover {
        background-color: rgba(0, 0, 0,0.1);
        border-radius: 50%;
    }
</style>