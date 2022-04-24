<p align = center>МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ

<p align = center>РОССИЙСКОЙ ФЕДЕРАЦИИ

<p align = center>ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ

<p align = center>«ВЯТСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»

<p align = center>Институт математики и информационных систем

<p align = center>Факультет автоматики и вычислительной техники

<p align = center>Кафедра систем автоматизации управления
<br>
<br>
<br>
<br>

<p align = right>Дата сдачи на проверку:

<p align = right>«___» __________ 2022 г.

<p align = right>Проверено:

<p align = right>«___» __________ 2022 г.
<br>
<br>
<br>
<br>
<br>

<p align = center>Отчет по лабораторной работе № 3

<p align = center>по дисциплине

<p align = center>«Web-программирование»

<br>
<br>
<br>
<br>

<p align = center>Разработал студент гр. ИТб-2301-01-00 ________________ /Кислицын И.А./

<p align = center>Проверил ст. преподаватель _________________ /Земцов М.А./

<p align = center>Работа защищена с оценкой «___________» «___» __________ 2022 г.

<br>
<br>
<br>
<br>

<p align = center>Киров 2022

<hr>
Цель:  провести тестирование отправки axios-запроса на mock-сервер

Задачи:

1. Организовать процесс работы над лабораторной работой
1. Сверстать блок регистрации
1. Создать mock-сервер в Postman
1. Отправить запрос на mock-сервер и получить ответ

Ход выполнения:

1. Организовать процесс работы над лабораторной работой

Для работы в репозитории _[ссылка на репозиторий](https://github.com/Ivan2567/WEB_2K)_ на сайте github.com была создана новая ветвь с названием Lab3.

2. Сверстать блок регистрации

<p align=center><img src="./img/l3_1.png" alt=""></p>

<p align = center>Рисунок 1 – Вход desctop

<p align=center><img src="./img/l3_2.png" alt=""></p>

<p align = center>Рисунок 2 – Регистрация desctop

3. Создать mock-сервер в Postman

В ходе выполнения работы с помощью Postman был создан Mock Server. Созданный Mock Server представлен на рисунке 3.

<p align=center><img src="./img/l3_2,4.png" alt=""></p>

<p align = center>Рисунок 3 – Mock Server

В рамках лабораторной работы были созданы два Post запроса.
В первом случае Post запрос используется для проверки введенного логина и пароля. Реализация запроса изображена на рисунке 4. Результаты его работы показаны на рисунках 5 и 6.

<p align=center><img src="./img/l3_2,5.png" alt=""></p>

<p align = center>Рисунок 4 – Post запрос

<p align=center><img src="./img/l3_3.png" alt=""></p>

<p align = center>Рисунок 5 – Удачный вход

<p align=center><img src="./img/l3_4.png" alt=""></p>

<p align = center>Рисунок 6 – Неудачный вход

Во втором случае Post запрос используется для проверки уникальности логина при регистрации. Реализация запроса изображена на рисунке 7. Результаты его работы показаны на рисунках 8 и 9.

<p align=center><img src="./img/l3_4,5.png" alt=""></p>

<p align = center>Рисунок 7 – Post запрос

<p align=center><img src="./img/l3_5.png" alt=""></p>

<p align = center>Рисунок 8 – Удачная регистрация

<p align=center><img src="./img/l3_6.png" alt=""></p>

<p align = center>Рисунок 9 – Неудачная регистрация

В компоненте reg предусмотрена проверка на совпадение введенных паролей
Листинг компонента reg представлен в приложении А.

Вывод: в ходе лабораторной работы было проведено тестирование отправки axios-запроса на mock-сервер.

<p align = center>Приложение А

<p align = center>(обязательное)

<p align = center>Листинг компонента reg.vue

```html
<template>
<div  class="container">
    <div class="form_block">
        <div class="login_block">
        <label>Логин:</label>
        <div class="login">
            <input id="login-input"  type="text" placeholder="Введите логин" required >
        </div>

        </div>
        <div class="login_block">
        <label>Пароль:</label>
        <div class="login">
            <input id="login-input2"  type="text" placeholder="Введите пароль" required >
        </div>
        </div>

        <div v-show="reg===true" class="login_block2">
        <label>Пароль:</label>
        <div class="login">
            <input id="login-input3"  type="text" placeholder="Повторите пароль" required >
        </div>
        </div>

        <div v-show="reg===true" class="btn">
        <input @click="regist" id="btn-input" type="button" value="Зарегистрироватся">
        </div>
        <div v-show="reg===false" class="btn">
        <input @click="aunt" id="btn-input" type="button" value="Войти">
        </div>
        <div class="btnblc" >
            <div class="btn">
            <input @click="regis" id="btn-input1" type="button" value="Регистрация">
            </div>  

            <div class="btn">
            <input @click="aun" id="btn-input2" type="button" value="Вход">
            </div>  
        </div>

    </div>
</div>
</template>

<script lang="ts">
import axios from "axios";
import { defineComponent } from 'vue';

export default defineComponent({
name: 'App',
data(){
    return{reg: true,}},
 components: {
},
methods:{
    regis()
    { 
        this.reg = true
    },
    aun()
    { 
        this.reg = false
    },

    regist() 
    {
        const regLogin: HTMLInputElement = document.getElementById("login-input") as HTMLInputElement;

        const pass: HTMLInputElement = document.getElementById("login-input2") as HTMLInputElement;

        const pass2: HTMLInputElement = document.getElementById( "login-input3") as HTMLInputElement;
        const config = {
          url: 'https://41eb137d-1101-4c0b-8468-f84aec186a3a.mock.pstmn.io/logcheck',
        };
        const data = {
          login: regLogin.value,
        };
        if (regLogin.value === "") {
          alert("Введите логин");
          return;
        }
        if (pass.value === "") {
          alert("Введите пароль");
          return;
        }
        if (pass2.value === "") {
          alert("Повторите пароль");
          return;
        }
        if (pass.value != pass2.value) {
          alert("Пароли не совпадают");
          return;
        }
        axios
          .post(config.url, data, {
            headers: { 'x-mock-match-request-body': true },
          })
         .then(
          (res: any) => {
            alert("Данный логин уже занят");
          },
        ).catch(
        (err: any) => {
          alert("Регистрация прошла успешно");
          });
    },
    aunt() 
    {
        const regLogin: HTMLInputElement = document.getElementById("login-input") as HTMLInputElement;

        const pass: HTMLInputElement = document.getElementById("login-input2") as HTMLInputElement;
        const config = {
          url: 'https://41eb137d-1101-4c0b-8468-f84aec186a3a.mock.pstmn.io/aunt',
        };
        const data = {
          login: regLogin.value, password: pass.value
        };
        if (regLogin.value === "") {
          alert("Введите логин");
          return;
        }
        if (pass.value === "") {
          alert("Введите пароль");
          return;
        }
        axios
          .post(config.url, data, {
            headers: { 'x-mock-match-request-body': true },
          })
         .then(
          (res: any) => {
            alert("Вы вошли");
          },
        ).catch(
        (err: any) => {
          alert("Неверный логин или пароль");
          });
    },

        }
});

</script>
<style>
#app {
font-family: Avenir, Helvetica, Arial, sans-serif;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
text-align: center;
color: #2c3e50;
margin-top: 60px;
}

.container {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
}


.form_block, .login_block {
    display: flex;
    justify-content: center;
    flex-direction: column;
    margin-bottom: 30px;
}

.login, .btn {

    text-align: center;
    width: 300px;
    position: relative;
}
.btn{margin-top: 1vh;}
 #login-input, #login-input2, #login-input3, #btn-input, #btn-input1, #btn-input2 {
    width: 100%;
    padding: 5px 0;
    height: 30px;
    line-height: 40px;
    text-indent: 10px;
    border-radius: 5px;
    border: 1px solid #999;
    font-size: 18px;

}

#btn-input, #btn-input1, #btn-input2 {
    width: 80%;
    padding: 5px 0;
    height: auto;
    line-height: 40px;
    text-indent: 10px;
    margin: 0 0 15px 0;
    border-radius: 5px;
    border: 1px solid #999;
    font-size: 18px;
}
.btnblc
{
    display: inline-block;
    background: #2c3e50;
}

@media (max-width: 580px) { 
    .container {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
}

</style>
```
