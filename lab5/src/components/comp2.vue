<template>
<div>
    
    <div class="main">
        <div class="frame">
            <div class="topbar">
                <div class="search">
                    <label>
                        <input type="text" placeholder="Search...">
                        <img src="../assets/lupa.png" alt="">
                    </label>
                </div>
                <div class="user"> 
                    <div class="usericon"> <img src="../assets/usericon.png" alt=""></div>
                    <div class="btn"><img src="../assets/btn.png" alt=""></div>
                </div>
            </div>
            <div class="title">
                    <div class="titletext">Your unfinished courses</div>
                    <div class="3dots"><img src="../assets/3dots.png" alt=""></div>
            </div>
            <div class="block1">
                <div><img src="../assets/unfin1.png" alt=""></div>
                <div><img src="../assets/unfin2.png" alt=""></div>
            </div>
            <div class="title">
                    <div class="titletext">Live lessons</div>
                    <div class="3dots"><img src="../assets/3dots.png" alt=""></div>
            </div>
            <div class="block2">
                <div><img src="../assets/live1.png" alt=""></div>
                <div><img src="../assets/live2.png" alt=""></div>
                <div><img src="../assets/live3.png" alt=""></div>
                <div><img src="../assets/live4.png" alt=""></div>
                <div><img src="../assets/live5.png" alt=""></div>
                <div><img src="../assets/live6.png" alt=""></div>
                <div><img src="../assets/live7.png" alt=""></div>
                <div><img src="../assets/rightarr.png" alt=""></div>
            </div>
        </div>
        </div>
    </div>
</template>

<script lang="ts" >

 import { defineComponent } from 'vue';

 export default defineComponent({
   name: 'comp2',
   components: {
   }
 });
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@500&display=swap');
*
{
    font-family: 'Roboto', sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
:root
{
    --blue: #503E9D;
    --white: #fff;
    --grey: #f5f5f5;
    --black1: #222;
    --black2: #999;

}
body
{
    min-height: 100vn;
    overflow-x: hidden;
}

.main
{
    position: absolute;
    width: calc(100% - 26%);
    left: 26%;
    height: 100%;
    min-height: 100vh; 
    background: var(--blue);
    transition: 0.5s;
    /* overflow: hidden; */
}
.frame
{
    /* position: absolute; */
    width: 98%;
    height: 94vh;
    background: var(--white);
    border-radius: 40px;
    margin-top: 2%;
    /* min-height: 500px;  */
    /* margin-bottom: 2%;   */
}
.topbar
{
    width: 100%;
    height: 130px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 4vw;


}
.user
{
    display: flex;
    align-items: center;
    padding: 0 10px;
}
.usericon
{
    padding: 0 20px;
}
.search
{
    position: relative;
    width: 800px;
    margin: 0 10px;
}
.search label
{
    position: relative;
    width: 100%;
    
}
.search label input
{
    width: 100%;
    height: 50px;
    border-radius: 15px;
    padding: 5px 10px;
    padding-left: 35px;
    outline: none;
    border: 0px solid var(--black2);
    font-size: 14px;
    background: var(--grey);
}
.search label img
{
    position: absolute;
    top: -2px;
    left: 10px;
    /* width: 4%;
    height: 100%; */
    width: 16px;
    height: 16px;
}
.usericon img
{
    width: 20px;
    height: 20px;

}
.btn img
{
    width: 50px;
    height: 50px;

}
.title
{
    width: 100%;
    display: flex;
    align-items: center;
    padding: 0 4.7vw;
    justify-content: space-between;
}
.titletext
{
    font-size: larger;
}
.block1 {
    /* margin-right: 2%; */
    width: 100%;
    height: 325px;
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fit, minmax(170px, 2fr));
    grid-template-rows: repeat(1, 300px);
}
.block1  div  img {
    width: 100%;
    height: 100%;
    object-fit: contain;
}
.block2 {
    width: 73vw;
    padding: 0 2vw;
    height: 155px;
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fit, minmax(100px, 8fr));
    grid-template-rows: repeat(8, 155px);
}
.block2  div  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

@media screen and (max-width: 1211px) 
{
    .main
    {
        height: 870px;
    }
        .frame
    {
        height: 850px;
    }
}
@media screen and (max-width: 476px) 
{
    .block1 
    {
        height: 625px;
    }
        .main
    {
        height: 1480px;
    }
        .frame
    {
        height: 1468px;
    }
}
/* @media screen and (max-width: 476px) 
{
    .block1 
    {
        height: 625px;
    }
} */
</style>