<template>
  <div id="app" class="app-background">
    <div class="q-pa-md">
      <div>
        <div class="alignItems">
          <!-- Exibe o componente DialogBoxRight após 1 segundo -->
          <DialogBoxRightLeft
            message="Eae Pai, me peguei aqui pensando sobre sua história, desde quando chegou aqui em São Paulo, tem que ter muita coragem para sair do outro lado do mundo e tentar ganhar a vida na terra da saudade"
          />
          <DialogBoxRightLeft
             v-if="this.showbox2"
            message="E a sua maior coragem deve ter sido a de enfrentar a sua saudade, saudade do seu seu pai, o vô Henrique, do sol, como mesmo já disse, naquela época quando chegou aqui, São paulo ainda era a terra da garoa , não a terra da saudade, eu tenho certeza que tem saudade da sua comida, e vive matando a saudade dela com a gente, cozinhando  várias coisas boa, saudade da sua rede. Quantas saudades você carrega Pai ? "
          />
          <dialogBoxImage :imageContent="ExpressoNordeste" v-if="showbox3"/>
          <DialogBoxRightLeft
           v-if="showbox4"
            message="Ao 17 anos o menino de quijingue foi explorando a quarta maior cidade do mundo, andando entre o centro e a periferia, e fazendo naquele momento sua morada o campo limpo, extremo sul, São paulo  "
          />
          <dialogBoxImage :imageContent="pracaRepublica" />
          <dialogBoxImage :imageContent="CampoLimpo" />

          <!-- Exibe o componente DialogBoxRightLeft após 2 segundos -->
          <DialogBoxRightLeft
            message="Depois de um tempo conseguiu conquistar o sonho de consumo de muitos na época dos anos 80, um fusquinha, e um black power"
          />
          <dialogBoxImage :imageContent="personagem08" />
          <DialogBoxRightLeft
            message="Mas com o tempo a responsa bateu na sua porta, e as prioridade de da  suporte para sua família foi maior e vendeu seu fusquinha na época do cruzeiro para da entrada em um terreno no jardim ângela , periferia da zona sul de São Paulo"
          />
          <dialogBoxImage :imageContent="escrituraTerreno" />
          <dialogBoxImage :imageContent="materia" />
          <DialogBoxRightLeft
            message="Lembro que foi construindo a casa , para sairmos do aluguel , e depois quando eu tinha 5 anos , todos nós mudamos para a casa, que lá construiremos nossas histórias"
          />
          <dialogBoxImage :imageContent="personagem96" />

          <DialogBoxRightLeft
            message="E depois de alguns anos , tijolo  por tijolo , com muita trabalho e esforço de toda família, fizemos daquele simples terreno , um lar , que aos domingos fazemos um churrasco na laje"
          />

          <dialogBoxImage :imageContent="personagem988" />
          <DialogBoxRightLeft
            message="Dia 16 de março de 2016 , as 10 e 26 da manhã, você se torna vô do Henrique Rodrigues, e seu olhar se ilumina"
          />

          <dialogBoxImage :imageContent="personagem995" />
          <dialogBoxImage :imageContent="imageContent" />
          <dialogBoxImage :imageContent="personagem90" />

          <DialogBoxRightLeft
            message="Mas eu ainda tô aqui perguntando Pai, quantas saudades você carrega ?"
          />
          <DialogBoxRightLeft
            message=" A primeira vez que te vi chorar foi no velório do vô Henrique , seu Pai , o ano era início de 2021. No começo de 2020 você estava cruzando a cidade para trazer ele para São Paulo , seria uma breve viagem , mas com a pandemia e tudo parado, vô Henrique ficou em São Paulo, esperando as coisas se normalizarem"
          />
          <DialogBoxRightLeft
            message=" Aos 97 anos Vo Henrique Partiu, seu coração  parou de bater no final do dia , e assim sua alma voou como uma pássaro, terminando sua história aqui na terra da saudade, onde seus filhos vieram para ganhar a vida "
          />
          <dialogBoxImage :imageContent="personagem09" />
          <DialogBoxRightLeft message="Quantas saudades você carrega Pai? " />
          <dialogBoxAudio :audioSrc="audio30" :imageProfile="imageProfile" />
          <DialogBoxRightLeft
            message="Em maio de 2024, você resolve voltar para sua terrinha, e matar um pouco da saudade, vendo os seus, comendo sua comida, andando pela cidade, e balançando na sua rede no quijingue"
          />
          <dialogBoxAudio :audioSrc="audio31" :imageProfile="imageProfile" />
          <MapComponent />

          <DialogBoxRightLeft
            message="Aos 72 anos, você cruza estados do Brasil Pai , sem olhar para trás, mas deixando saudade a cada áudio mandado"
          />

          <dialogBoxAudio :audioSrc="audio32" :imageProfile="imageProfile" />

          <DialogBoxRightLeft
            message="Imagino que muitas vezes está de imigrante nessa terra foi difícil, ter construído essa cidade e recebido tão pouco de volta, foi muito difícil, mas valeu por tudo, me ensina e me ensinou muito "
          />

          <dialogBoxAudio :audioSrc="audio33" :imageProfile="imageProfile" />

          <DialogBoxRightLeft
            message="Meu anjo da guarda que eu posso tocar "
          />

          <dialogBoxAudio :audioSrc="audio34" :imageProfile="imageProfile" />

          <DialogBoxRightLeft
            message="Meu anjo da guarda que eu posso tocar "
          />
          <dialogBoxImage :imageContent="personagem70" />
          <dialogBoxImage :imageContent="personagem60" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MapComponent from "./components/map.vue";
// import DialogBoxRight from "./components/dialogBoxRight.vue";
import DialogBoxRightLeft from "./components/dialogBoxLeft.vue";
import dialogBoxAudio from "./components/dialogBoxAudio.vue";
import dialogBoxImage from "./components/dialogBoxImage.vue";

export default {
  name: "App",
  components: {
    MapComponent,
    // DialogBoxRight,
    DialogBoxRightLeft,
    dialogBoxAudio,
    dialogBoxImage,
  },
  data() {
    return {
      audio30: require("@/assets/audio/audio30.mp3"),
      audio31: require("@/assets/audio/audio31.mp3"),
      audio32: require("@/assets/audio/audio32.mp3"),
      audio33: require("@/assets/audio/audio33.mp3"),
      audio34: require("@/assets/audio/audio34.mp3"),
      imageProfile: require("@/assets/image/perfilPersonagem02.jpeg"),
      imageContent: require("@/assets/image/perfilPersonagem02.jpeg"),
      ExpressoNordeste: require("@/assets/image/expressoNordest.jpg"),
      pracaRepublica: require("@/assets/image/pracaRepublica.jpg"),
      CampoLimpo: require("@/assets/image/campoLimpo.jpg"),
      personagem08: require("@/assets/image/personagem08.jpeg"),
      escrituraTerreno: require("@/assets/image/escritura-terreno.jpg"),
      materia: require("@/assets/image/materia1.png"),
      personagem96: require("@/assets/image/personagem96.jpeg"),
      personagem988: require("@/assets/image/personagem988.jpeg"),
      personagem995: require("@/assets/image/personagem995.jpeg"),
      personagem90: require("@/assets/image/personagem90.jpeg"),
      personagem09: require("@/assets/image/personagem09.jpeg"),
      personagem60: require("@/assets/image/personagem60.jpeg"),
      personagem70: require("@/assets/image/personagem70.jpeg"),
      showbox2: false,
      showbox3: false,
      showbox4: false,
      
      showDialogBoxAudio: false,
      showDialogBoxImage: false,
      showMapComponent: false,
    };
  },
  mounted() {
    setTimeout(() => {
      this.showbox2 = true;
    }, 17000); // 2 segundos

    setTimeout(() => {
      this.showbox3= true;
    }, 51000); // 3 segundos

    setTimeout(() => {
      this.showbox4 = true;
    }, 53000); // 4 segundos

    setTimeout(() => {
      this.showMapComponent = true;
    }, 50000); // 5 segundos
  },
};
</script>

<style scoped>
.app-background {
  background-image: url("assets/image/backgroundDark.jpeg");
  min-height: 1050px;
}

.alignItems {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 20px;
}
</style>
