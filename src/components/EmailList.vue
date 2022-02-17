<script setup>
import TabList from './TabList.vue'
import EmailRow from './EmailRow.vue'
</script>

<template>
    <div class="email-list">
        <div class="email-settings">
            <div class="email-settings__left">
                <span class="material-icons">check_box_outline_blank</span>
                <span class="material-icons">refresh</span>
                <span class="material-icons">more_vert</span>
            </div>

            <div class="email-settings__right">
                <span class="material-icons">chevron_left</span>
                <span class="material-icons">chevron_right</span>
            </div>
        </div>

        <div class="email-list__tab">
            <TabList />
        </div>

        <div class="email-list__row">
            <EmailRow />
        </div>
    </div>
</template>



<style scoped>
    .email-list{
        flex: 1;
        overflow: scroll;
    }
    .email-settings{
        position: sticky;
        top: 10px;
        display:flex;
        align-items:center;
        justify-content:space-between;
        box-shadow: 0px 2px whitesmoke;
    }
    .email-settings__right{
        padding-right: 20px;
    }
    .email-settings__left{ 
        padding-left: 20px;
    }

    .email-list__tab{
        display: flex;
        border-bottom: 1px solid whitesmoke;
        background-color: #fff;
        box-shadow: 0px 2px whitesmoke;
    }
    .material-icons:hover {
        background-color: rgba(0, 0, 0,0.1);
        border-radius: 50%;
    }
    
</style>