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
// import step2  from '../../src/components/Step_2.vue'
//двустороннее привязывание

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