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
          <dialogBoxImage 
            v-if="showbox5" 
            :imageContent="pracaRepublica" />
          <dialogBoxImage 
             v-if="showbox6"  :imageContent="CampoLimpo" />

          <!-- Exibe o componente DialogBoxRightLeft após 2 segundos -->
          <DialogBoxRightLeft
            v-if="showbox7"
            message="Depois de um tempo conseguiu conquistar o sonho de consumo de muitos na época dos anos 80, um fusquinha, e um black power"
          />
          <dialogBoxImage v-if="showbox8" :imageContent="personagem08" />
          <DialogBoxRightLeft
           v-if="showbox9"
            message="Mas com o tempo a responsa bateu na sua porta, e as prioridade de da  suporte para sua família foi maior e vendeu seu fusquinha na época do cruzeiro para da entrada em um terreno no jardim ângela , periferia da zona sul de São Paulo"
          />
          <dialogBoxImage v-if="showbox10" :imageContent="escrituraTerreno" />
          <dialogBoxImage v-if="showbox11" :imageContent="materia" />
          <DialogBoxRightLeft
            v-if="showbox12"
            message="Lembro que foi construindo a casa , para sairmos do aluguel , e depois quando eu tinha 5 anos , todos nós mudamos para a casa, que lá construiremos nossas histórias"
          />
          <dialogBoxImage v-if="showbox13" :imageContent="personagem96" />

          <DialogBoxRightLeft
          v-if="showbox14"
            message="E depois de alguns anos , tijolo  por tijolo , com muita trabalho e esforço de toda família, fizemos daquele simples terreno , um lar , que aos domingos fazemos um churrasco na laje"
          />

          <dialogBoxImage  v-if="showbox15" :imageContent="personagem988" />
          <DialogBoxRightLeft
           v-if="showbox16"
            message="Dia 16 de março de 2016 , as 10 e 26 da manhã, você se torna vô do Henrique Rodrigues, e seu olhar se ilumina"
          />

          <dialogBoxImage v-if="showbox17"  :imageContent="personagem995" />
          <dialogBoxImage v-if="showbox18" :imageContent="imageContent" />
          <dialogBoxImage v-if="showbox19" :imageContent="personagem90" />

          <DialogBoxRightLeft
           v-if="showbox20"
            message="Mas eu ainda tô aqui perguntando Pai, quantas saudades você carrega ?"
          />
          <DialogBoxRightLeft
          v-if="showbox21"
            message=" A primeira vez que te vi chorar foi no velório do vô Henrique , seu Pai , o ano era início de 2021. No começo de 2020 você estava cruzando a cidade para trazer ele para São Paulo , seria uma breve viagem , mas com a pandemia e tudo parado, vô Henrique ficou em São Paulo, esperando as coisas se normalizarem"
          />
          <DialogBoxRightLeft
          v-if="showbox22"
            message=" Aos 97 anos Vo Henrique Partiu, seu coração  parou de bater no final do dia , e assim sua alma voou como uma pássaro, terminando sua história aqui na terra da saudade, onde seus filhos vieram para ganhar a vida "
          />
          <dialogBoxImage v-if="showbox23" :imageContent="personagem09" />
          <DialogBoxRightLeft v-if="showbox24" message="Quantas saudades você carrega Pai? " />
          <dialogBoxAudio v-if="showbox25"  :audioSrc="audio30" :imageProfile="imageProfile" />
          <DialogBoxRightLeft
            v-if="showbox26"
            message="Em maio de 2024, você resolve voltar para sua terrinha, e matar um pouco da saudade, vendo os seus, comendo sua comida, andando pela cidade, e balançando na sua rede no quijingue"
          />
          <dialogBoxAudio v-if="showbox27" :audioSrc="audio31" :imageProfile="imageProfile" />
          <MapComponent v-if="showbox28" />

          <DialogBoxRightLeft
           v-if="showbox29"
            message="Aos 72 anos, você cruza estados do Brasil Pai , sem olhar para trás, mas deixando saudade a cada áudio mandado"
          />

          <dialogBoxAudio  v-if="showbox30" :audioSrc="audio32" :imageProfile="imageProfile" />

          <DialogBoxRightLeft
           v-if="showbox31"
            message="Imagino que muitas vezes está de imigrante nessa terra foi difícil, ter construído essa cidade e recebido tão pouco de volta, foi muito difícil, mas valeu por tudo, me ensina e me ensinou muito "
          />

          <dialogBoxAudio  v-if="showbox32" :audioSrc="audio33" :imageProfile="imageProfile" />

          <DialogBoxRightLeft
            v-if="showbox33"
            message="Meu anjo da guarda que  posso tocar "
          />

          <dialogBoxAudio v-if="showbox34" :audioSrc="audio34" :imageProfile="imageProfile" />

          <DialogBoxRightLeft
           v-if="showbox35"
            message="Hoje somos todos a continuação do seu sonho e dos que vieram antes de você  "
          />
          <dialogBoxImage  v-if="showbox36"  :imageContent="personagem70" />
          <dialogBoxImage v-if="showbox37"  :imageContent="personagem60" />
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
      showbox5: false,
      showbox6: false,
      showbox7: false,
      showbox8: false,
      showbox9: false,
      showbox10: false,
      showbox11: false,
      showbox12: false,
      showbox13: false,
      showbox14: false,
      showbox15: false,
      showbox16: false,
      showbox17: false,
      showbox18: false,
      showbox19: false,
      showbox20: false,
      showbox21: false,
      showbox22: false,
      showbox23: false,
      showbox24: false,
      showbox25: false,
      showbox26: false,
      showbox27: false,
      showbox28: false,
      showbox29: false,
      showbox30: false,
      showbox31: false,
      showbox32: false,
      showbox33: false,
      showbox34: false,
      showbox35: false,
      showbox36: false,
      showbox37: false,
    };
  },
  mounted() {
    setTimeout(() => {
      this.showbox2 = true;
    }, 17000); 

    setTimeout(() => {
      this.showbox3= true;
    }, 51000); 

    setTimeout(() => {
      this.showbox4 = true;
    }, 53000);
    
    setTimeout(() => {
      this.showbox5 = true;
    }, 60000); 
    setTimeout(() => {
      this.showbox6 = true;
    }, 61000);
    setTimeout(() => {
      this.showbox7 = true;
    }, 68000);
    setTimeout(() => {
      this.showbox8 = true;
    }, 70000);
    setTimeout(() => {
      this.showbox9 = true;
    }, 80000);
    setTimeout(() => {
      this.showbox10 = true;
    }, 82000);
    setTimeout(() => {
      this.showbox11 = true;
    }, 83000);
    setTimeout(() => {
      this.showbox12 = true;
    }, 97000);
    setTimeout(() => {
      this.showbox13 = true;
    }, 99000);
    setTimeout(() => {
      this.showbox14 = true;
    }, 109000);
    setTimeout(() => {
      this.showbox15 = true;
    }, 109000);
    setTimeout(() => {
      this.showbox16 = true;
    }, 122000);
    setTimeout(() => {
      this.showbox17 = true;
    }, 124000);
    setTimeout(() => {
      this.showbox18 = true;
    }, 125000);
    setTimeout(() => {
      this.showbox19 = true;
    }, 126000);
    setTimeout(() => {
      this.showbox20 = true;
    }, 128000);
    setTimeout(() => {
      this.showbox21 = true;
    }, 138000);
    setTimeout(() => {
      this.showbox22 = true;
    }, 160000);
    setTimeout(() => {
      this.showbox23 = true;
    }, 168000);
    setTimeout(() => {
      this.showbox24 = true;
    }, 182000);
    setTimeout(() => {
      this.showbox25 = true;
    }, 186000);
    setTimeout(() => {
      this.showbox26 = true;
    }, 206000);
    setTimeout(() => {
      this.showbox27 = true;
    }, 216000);
    setTimeout(() => {
      this.showbox28 = true;
    }, 216000);
    setTimeout(() => {
      this.showbox29 = true;
    }, 220000);
    setTimeout(() => {
      this.showbox30 = true;
    }, 226000);
    setTimeout(() => {
      this.showbox31 = true;
    }, 236000);
    setTimeout(() => {
      this.showbox32 = true;
    }, 239000);
    setTimeout(() => {
      this.showbox33 = true;
    }, 266000);
    setTimeout(() => {
      this.showbox34 = true;
    }, 270000);
    setTimeout(() => {
      this.showbox35 = true;
    }, 273000);
    setTimeout(() => {
      this.showbox36 = true;
    }, 278000);
    setTimeout(() => {
      this.showbox37 = true;
    }, 279000);
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
