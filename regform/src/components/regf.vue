<template>
<div class="container">
<div class= "img_block"><img src="../assets/mariby-the-sea-hot.gif" alt=""></div>
    <div class="form_block">
        <div class="login_block">
        <label>Логин:</label>
        <div class="login">
            <input id="login-input" type="text" placeholder="Введите логин" >
        </div>
        </div>

        <div class="password_block">
        <label>Пароль:</label>
        <div class="password">
            <input type="password" id="password-input" placeholder="Введите пароль" name="password">
            <button v-on:click="showOrHide" id="password-control" class="password-control"></button>
        </div>
        </div>

        <div class="btn">
        <input id="btn-input" type="button" value="Отправить">
        </div>
    </div>
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
name: 'App',
components: {
},
methods:{
            showOrHide: function(){
                const input = document.getElementById('password-input');
                const image = document.getElementById('password-control');
                
                if (input != null && image != null) {
                if (input.getAttribute('type') == 'password') {
                    input.setAttribute('type', 'text');
                    image.classList.add('view');
                }
                else {
                    input.setAttribute('type', 'password');
                    image.classList.remove('view');
                }
                return false;
                }
            return false;
            }  
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

.img_block {
    padding: 20px;
}

.form_block, .login_block, .password_block {
    display: flex;
    justify-content: center;
flex-direction: column;
margin-bottom: 30px;
}

.password, .login, .btn {
    text-align: center;
    width: 300px;
    position: relative;
}
#password-input, #login-input, #btn-input {
    width: 100%;
    padding: 5px 0;
    height: 30px;
    line-height: 40px;
    text-indent: 10px;
    border-radius: 5px;
    border: 1px solid #999;
    font-size: 18px;
}

#btn-input {
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

.password-control {
    position: absolute;
    top: 11px;
    right: 6px;
    display: inline-block;
    width: 20px;
    height: 20px;
    background: url(https://snipp.ru/demo/495/no-view.svg) 0 0 no-repeat;
    border: 0;
}
.password-control.view {
    background: url(https://snipp.ru/demo/495/view.svg) 0 0 no-repeat;
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