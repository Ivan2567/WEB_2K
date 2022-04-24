<p align = center>МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ
<p align = center>РОССИЙСКОЙ ФЕДЕРАЦИИ
<p align = center>ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ
<p align = center>«ВЯТСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»
<p align = center>Институт математики и информационных систем
<p align = center>Факультет автоматики и вычислительной техники
<p align = center>Кафедра систем автоматизации управления
<p align = right>Дата сдачи на проверку:
<p align = right>«___» ________________ 2022 г.
<p align = right>Проверено:
<p align = right>«___» ________________ 2022 г.
<p align = center >Отчет по лабораторной работе № 4
<p align = center>по дисциплине
<p align = center>«Web-программирование»
<br/>
<br/>
<br/>
<br/>
<br/>

<p align = right>Разработал студент гр. ИТб-2301-01-00 __________________ /Морозов И.В./
<p align = right>Проверил преподаватель _________________ /Земцов М.А./
<p align = right>Оценка работы	«___________» 
«____»_____________ 2022 г.
<br/>
<br/>
<br/>
<br/>
<br/>
<p align = center>Киров 2022
<br/><br/>

<p align = justify style="text-indent: 25px;">Цель: создать макет дашборда с применением компонентов фреймворка
<br/><br/>

<p align = justify style="text-indent: 25px;">
Задачи:

1. Организовать процесс работы над лабораторной работой
1. Реализовать верстку
1. Сделать адаптив для мобильных устройств
<br/><br/>

<p align = justify style="text-indent: 25px;">Ход выполнения:

1. Организовать процесс работы над лабораторной работой.
<p align = justify style="text-indent: 25px;">
Для работы в репозитории _[ссылка на репозиторий](https://github.com/Ivan2567/WEB_2K)_ на сайте github.com была создана новая ветвь с названием Lab4.

2. Реализовать верстку
<p align = justify style="text-indent: 25px;">Образец дашборда предствален на рисунке 1. Конечный результат верстки отображен на рисунке 2. Листинг основных компонентов приведен в приложениях А, Б.
<br><br>

<p align=center><img src=./Img/4_1.png></p>
<p align = center>Рисунок 1 - Макет дашборда
<br><br>
<p align=center><img src=./Img/4_2.png></p>
<p align = center>Рисунок 2 - Образец готовой верстки
<br><br>


3. Сделать адаптив для мобильных устройств
<p align = justify style="text-indent: 25px;">
В ходе выполнения работы были сделана адаптация страницы под мобильные устройства.

<p align=center><img src=./Img/4_3.png></p>
<p align = center>Рисунок 6 - Адаптация для телефонов
<br><br>


<p align = justify style="text-indent: 25px;">Вывод: в ходе выполнения работы были повторены навыки верстики сайтов, опробован метод верстки с применением компонентов.
<br><br>


<p align = center>Приложение А

<p align = center>(обязательное)
<p align = center> Листинг компонента comp

```html
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
```

<br><br>

<p align = center>Приложение Б

<p align = center>Листинг компонента comp2

```html
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
```

