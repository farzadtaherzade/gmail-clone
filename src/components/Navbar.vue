<script setup>

</script>

<template>
    <header class="header">
        <div class="left-content">
            <span class="material-icons">menu</span>
            <img src="../assets/logo_gmail_lockup_default_1x_r2.png" alt="">
        </div>

        <div class="conter-content">
            <i class="fa-solid fa-magnifying-glass"></i>
            <input type="search" name="search" id="search" placeholder="Search mail">
            <span class="material-icons">tune</span>
        </div>

        <div class="right-content">
            <span class="material-icons">help_outline</span>
            <span class="material-icons">settings</span>
            <span class="material-icons">apps</span>
            <span class="material-icons">account_circle</span>
        </div>
    </header>
</template>

<style scoped>
@import '../assets/base.css';

.header{
    width: 100%;
    background-color: #fff;
    padding: 8px;
    box-shadow: 0px 2px whitesmoke;
    display:flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: nowrap;
}
.left-content{
    display: flex;
    align-items: center;
}
.left-content span {
    cursor: pointer;
    padding: 8px;
    margin-right:10px;
    font-size: 26px;
}
.left-content img{
    object-fit: contain;
    height: 40px;
}
.conter-content{
    position: relative;
    display: flex;
    align-items: center;
    flex: .7;
    background-color: whitesmoke;
    padding: 10px;
    border-radius:7px;
    /* margin-right:190px; */
    color: #000;
}
#search[type="search"]{
    position: relative;
    width: 100%;
    border: none;
    padding: 10px;
    outline: none;
    font-size: medium;
    background-color:transparent;
}
#search[type="search"]::-webkit-search-decoration:hover,
#search[type="search"]::-webkit-search-cancel-button:hover {
    cursor:pointer;
}
#search[type="search"]{font-size:15px; color: #000;}
#search[type="search"]::-webkit-search-cancel-button,
#search[type="search"]::-webkit-search-decoration{
    position: absolute;
    right: 50px;
    -webkit-appearance: none;
    font-size:100px;

    background: url('../assets/close_black_24dp.svg');
    background-repeat: no-repeat;
    background-position: center;
    height: 20px;
    width: 20px;
    opacity: .6;
}

.conter-content span{
    position: absolute;
    right: 20px;
    padding: 10px;
    cursor: pointer;
}

.right-content{
    display: flex;
    flex-wrap: nowrap;
    padding-right:20px;
}
.right-content span{ padding:10px; cursor: pointer; }

.conter-content i{
    padding: 12px;
    cursor: pointer;
}

.material-icons{
    background-color: none;
}

.material-icons:hover , .conter-content i:hover {
    background-color: rgba(0, 0, 0,0.1);
    border-radius: 50%;
    transition: .01s ;
}

@media (max-width: 768px) {
    .left-content img {
        object-fit: contain;
        height: 35px;
    }
    .conter-content{
        flex: .9;
    }
}
@media (max-width: 560px) {
    .left-content img {
        display: none;
    }
    .conter-content{
        flex: 1;
    }
    .right-content span { 
        display: none;
    }
}

</style>
