<template>
<div>
<div class="body-layout">
    <h1> Pizzas </h1>
        <div v-for="(slide, index) in slides" lines="none" :key="index">
            <img :src="baseAssetsImages + slide">
        </div>

    <ion-list>
          <ion-list-header> Salgadas</ion-list-header>

          <ion-item>
            <ion-avatar slot="start">
             <img :src="baseAssetsImages + imgSabores[2]">
            </ion-avatar>
            <ion-label>
              <h2>Mussarela</h2>
              <p>Tomates, queijo mussarela e majericão.</p>
            </ion-label>
          </ion-item>

          <ion-item>
            <ion-avatar slot="start">
             <img :src="baseAssetsImages + imgSabores[1]">
            </ion-avatar>
            <ion-label>
              <h2>Napolitana</h2>
              <p>Parmesão, queijo, tomates, orégano e alho.</p>
            </ion-label>
          </ion-item>

         <ion-item>
            <ion-avatar slot="start">
             <img :src="baseAssetsImages + imgSabores[0]">
            </ion-avatar>
            <ion-label>
              <h2>Portuguesa</h2>
              <p>Mussarela, tiras de presunto, cebola e azeitonas verdes e cream cheese.</p>
            </ion-label>
          </ion-item>

          <ion-item>
            <ion-avatar slot="start">
             <img :src="baseAssetsImages + imgSabores[1]">
            </ion-avatar>
            <ion-label>
              <h2>Frango</h2>
              <p>Frango desfiado e tomate.</p>
            </ion-label>
          </ion-item>         
    </ion-list>

      <ion-list>
          <ion-list-header> Doces</ion-list-header>

          <ion-item>
            <ion-avatar slot="start">
             <img :src="baseAssetsImages + imgSabores[2]">
            </ion-avatar>
            <ion-label>
              <h2>Brigadeiro</h2>
              <p>Creme de chocolate.</p>
            </ion-label>
          </ion-item>

          <ion-item>
            <ion-avatar slot="start">
             <img :src="baseAssetsImages + imgSabores[1]">
            </ion-avatar>
            <ion-label>
              <h2>Romeu e Julieta</h2>
              <p>Queijo branco com goiabada.</p>
            </ion-label>
          </ion-item>

         <ion-item>
            <ion-avatar slot="start">
             <img :src="baseAssetsImages + imgSabores[0]">
            </ion-avatar>
            <ion-label>
              <h2>Banana com Doce de Leite</h2>
              <p>Banana com creme de doce de leite.</p>
            </ion-label>
          </ion-item>

          <ion-item>
            <ion-avatar slot="start">
             <img :src="baseAssetsImages + imgSabores[1]">
            </ion-avatar>
            <ion-label>
              <h2>Marshmellow</h2>
              <p>Marshmellow com caramelo salgado.</p>
            </ion-label>
          </ion-item>         
    </ion-list>
</div>

    <ion-fab vertical="bottom" horizontal="end" slot="fixed" @click="finalizarPedido">
        <ion-fab-button>
        <ion-icon :icon="arrowForwardCircle"></ion-icon>
        </ion-fab-button>
    </ion-fab>

    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { arrowForwardCircle } from "ionicons/icons";

export default defineComponent({
    name: "MenuCardapio",
    components : {
    },
    data() {
        return {
            baseAssetsImages: "./assets/images/",
            slides: ["slide-pizza-1.jpg"],
            imgSabores : ["slide-pizza-1.jpg","slide-pizza-2.jpg","slide-pizza-3.jpg"],
            arrowForwardCircle: arrowForwardCircle
        }
    },
    methods: {
    async finalizarPedido(){
        alert("Deseja finalizar o pedido?");
    }
    }

});
</script>

<style scoped>
h1{
    text-align: left;
}

img {
    width: 370px;
    border-radius: 15px;
}
ion-footer{
    position: fixed;
}
ion-fab{
    position: fixed;
    bottom: 10px;
    right: 5px;
}
</style>
