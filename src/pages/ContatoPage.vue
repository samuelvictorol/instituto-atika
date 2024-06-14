<template>
    <q-page class="relative bg-accent column items-center animate__animated animate__fadeIn animate__slow">
        <div class="text-h4 text-primary text-center q-py-md">Contato ✉️</div>
        <div class="q-mt-md column q-gutter-y-md justify-center items-center form-contato w80">
            <q-input maxlength="100" outlined class="w100 bg-white" label="Nome Completo*"/>
            <q-input maxlength="100" outlined class="w100 bg-white" label="Email*" placeholder="seuemail@email.com"/>
            <q-input maxlength="400" outlined class="w100 bg-white" type="textarea" label="Mensagem*"/>
            <q-btn color="primary" label="Enviar mensagem" icon="send" class="w100 q-mt-md"/>
        </div>
        <div class="absolute-bottom w100 bg-accent q-py-md row justify-center ">
            <a target="_blank" href="https://www.instagram.com/institutoatika/">
                <img
                class="rounded-borders"
                  style="width:140px"
                  alt="instagram logo"
                  src="~assets/insta.png"
                >
              </a>
          </div>
    </q-page>
</template> 

<script setup>
import { ref } from 'vue';


</script>

<style scoped>
@media screen {
    .form-contato {
        max-width: 500px;
    }
}
</style>