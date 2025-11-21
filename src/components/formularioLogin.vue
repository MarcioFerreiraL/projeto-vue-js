<template>
    <div :class="formStyle">
        <div>
            <label>Tipo Usuario</label>
        </div>
        <div>
            <select v-model="valueSelection">
                <option value="">Escolha</option>
                <option value="Administrador">Administrador</option>
                <option value="Atendente">Atendente</option>
                <option value="Tecnico">Tecnico</option>
                <option value="Cliente">Cliente</option>
            </select>
            {{ valueSelection }}
        </div>
        <div>
            <form action="submit"></form>
            <label >CPF</label> <br>
            <input 
            type="text"
            v-model="valueCpf"
            @keyup.enter="onClickButton"
            >
            <button @click="onClickButton">Enviar</button>
        </div>
        {{ valueCpf }}
    </div>
</template>

<script>
    export default {
        formStyle: 'formStyle',
        data () {
            return {
                valueCpf: '',
                valueSelection: ''
            }
        },
        methods: {
            onClickButton() {
                console.log('clicado')
            }
        }
    }
</script>

<style>
    template {
        align-items: center;
    }
    .formStyle {
        font-family: Helvetica;
        color: blue;
    }
</style>