<template>
    <form class="form">
        <h2 class="form__title">Inicia sesión</h2>
        <p class="form__paragraph">Aun no tienes una cuenta? <a href="#" class="form__link">Click aqui</a></p>

        <div class="form__container">
            <div class="form__group">
                <input type="text" id="name" class="form__input" placeholder=" ">
                <label for="name" class="form__label">Nombre:</label>
                <span class="form__line"></span>
            </div>
            <div class="form__group">
                <input type="text" id="lastName" class="form__input" placeholder=" ">
                <label for="user" class="form__label">Usuario:</label>
                <span class="form__line"></span>
            </div>
            <div class="form__group">
                <input type="text" id="password" class="form__input" placeholder=" ">
                <label for="password" class="form__label">Contraseña:</label>
                <span class="form__line"></span>
            </div>

            <input type="submit" class="form__submit" value="Entrar">
        </div>
    </form>
</template>

<script>

</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:ital,wght@0,100..700;1,100..700&display=swap');

body {
    margin: 0;
    padding: 0;
    font-family: 'Roboto', sans-serif;
    background-color: #e5e5f7;
    opacity: 0.7;
    background-image: radial-gradient(#36e3c6 0.5px, #e5e5f7 0.5px);
    background-size: 10px 10px;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.a{
    display: flex;
    justify-content: center;
}

.form {
    background-color: #fff;
    margin: auto;
    width: 90%;
    max-width: 400px;
    padding: 4.5em 3em;
    border-radius: 10px;
    box-shadow: 0 5px 10px -5 rgb(0, 0, 0);
    text-align: center;
}

.form__title{
    font-size: 2rem;
    margin-bottom: .5em;
}

.form__link{
    font-weight: 400;
    color: rgb(0, 0, 0);
}

.form__container{
    margin-top: 3em;
    display: grid;
    gap: 2em;
}

.form__group{
    position: relative; 
    --color: #5757577;
}

.form__input{
    width: 100%;
    background: none;
    color: #706c6c;
    font-size: 1rem;
    padding: 2em .3em;
    border: none;
    outline: none;
    border-bottom: 1px solid var(--color);
    font-family: 'Roboto', sans-serif;
}

.form__input:focus + .form__label, .form__input:not(:placeholder-shown) + .form__label{
    transform: translateY(-12px) scale(.7);
    transform-origin: left top;
    color: #3866f2
}

.form__label{
    color: var(--color);
    cursor: pointer;
    position: absolute;
    top: 0;
    left: 10px;
    transform: translateY(10px);
    transition: transform .5s,
    color .3s;
}

.form__submit{
    background: #3866f2;
    color: #fff;
    font-family: 'Roboto', sans-serif;
    font-weight: 300;
    font-size: 1rem;
    padding: .8em 4em;
    border: none;
    border-radius: .5em;
}

.form__line{
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 1px;
    background-color: #3866f2;
    transform: scale(0);
    transform: left bottom;
}

.form__input:focus ~ .form__label, .form__input:not(:placeholder-shown) + .form__label{
    transform: scale(1);
}
</style>