<template>
  <div>
    <div class="home">
      <h1>Bem vindo ao <br> Roberto Manshi </h1>
    </div> 
      <Cardinfo 
        text_title:="Tratamento especial"
        text_content="Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado."
        back_color="black"
        text_color="white"
        :imgs = "my_imgs"
      />
  </div>
</template>

<script>

import Cardinfo from '../components/Cardinfo.vue'

export default {
    name: 'Home',
    components: {
      Cardinfo
    },
    data() {
      return {
        my_imgs: []
      }
    },
    methods: {
      async getImagesBackend(){
        const request = await fetch('http://localhost:3000/imgback');
        const jsonData = await request.json();
        console.log(jsonData)
      }
    },
    mounted() {
      this.getImagesBackend()
    } 
};
</script>


<style scoped src="./Home.css">

</style>