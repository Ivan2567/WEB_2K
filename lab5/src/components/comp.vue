<template>
<div>
    <div class="container">
    <div class="navig">
        <ul>
            <li>
                <a href="#">
                    <span class="icon"><img src="../assets/Group.png" alt=""></span>
                    <span class="title"></span>
                </a>
            </li> 
            <li>
                <a href="#">
                    <span class="icon"><img src="../assets/menu.png" alt=""></span>
                    <span class="title">Home</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span class="icon"><img src="../assets/prog.png" alt=""></span>
                    <span class="title">Progress</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span class="icon"><img src="../assets/mess.png" alt=""></span>
                    <span class="title">Messages</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span class="icon"><img src="../assets/set.png" alt=""></span>
                    <span class="title">Settings</span>
                </a>
            </li>
        </ul>
    </div>
    </div>
</div>
</template>

<script lang="ts" >

 import { defineComponent } from 'vue';
 //import brand from '../assets/logo.png';
// import comp from './components/comp.vue';

 export default defineComponent({
   name: 'comp',
   components: {
//     comp logo: foot1;
        //br: brand,
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
    --black1: #999;
    --ong: #FB6D3A;

}
body
{
    min-height: 100vn;
    overflow-x: hidden;
}
.container
{
    position: relative;
    width: 100%;

}
.navig
{
    position: fixed;
    width: 26%;
    height: 100%;
    background: var(--blue);
    border-left: 10px solid var(--blue) ;
    transition: 0.5s;
    overflow: hidden;
}
.navig ul 
{
    position: absolute;
    top:0;
    left: 0;
    width: 100%;
}
.navig ul  li
{
    position: relative;
    width: 100%;
    list-style: none;
    border-top-left-radius: 30px;
    border-bottom-left-radius: 30px;
}
.navig ul  li:hover
{
    background: var(--white);
}
.navig ul  li:nth-child(1)
{
    margin-top: 53px;
    margin-bottom: 80px;
    pointer-events: none;
    margin-left: 5vw;
} 
.navig ul  li:nth-child(2)
{
    margin-left: 3.5vw;
}
 .navig ul  li:nth-child(3)
{
    margin-left: 3.5vw;
}
.navig ul  li:nth-child(4)
{
   margin-left: 3.5vw;
}
.navig ul  li:nth-child(5)
{
    margin-left: 3.5vw;
} 
.navig ul li a
{
    position: relative;
    display: block;
    width: 100%;
    display: flex;
    text-decoration: none;
    color: var(--white);
    
}
.navig ul li:hover a
{
     color: var(--ong);
}
.navig ul li a .icon
{
    position: relative;
    display: block;
    min-width: 60px;
    height: 60px;
    line-height: 70px;
    top: 1px;
    text-align: center;
    
}
.navig ul  li a .title
{
    position: relative;
    display: block;
    padding: 0 25px;
    height: 60px;
    top: 0px;
    line-height: 60px;
    text-align: start;
    white-space: nowrap;
    font-size: 120%;
}
.navig ul li:hover a::before
{
    content: '';
    position: absolute;
    right: 0;
    top: -50px;
    width: 50px;
    height: 50px;
    background: transparent;
    border-radius: 50%;
    box-shadow: 35px 35px 0 10px var(--white);
    pointer-events: none;
    margin-right: 3.5vw;
}
.navig ul li:hover a::after
{
    content: '';
    position: absolute;
    right: 0;
    bottom: -50px;
    width: 50px;
    height: 50px;
    background: transparent;
    border-radius: 50%;
    box-shadow: 35px -35px 0 10px var(--white);
    pointer-events: none;
    margin-right: 3.5vw;
}
</style>
