<template>
<div class="body-layout">
<ion-card>
    <ion-card-header>
        <ion-card-subtitle>Casa</ion-card-subtitle>
    </ion-card-header>

    <ion-card-content t>
        Rua Roberto Justino, 192 - Santos, São Paulo
    </ion-card-content>
</ion-card>

<ion-card>
    <ion-card-header>
        <ion-card-subtitle>Trabalho</ion-card-subtitle>
    </ion-card-header>

    <ion-card-content t>
        Rua Expedicionários, 15400 - Santos, São Paulo
    </ion-card-content>
</ion-card>
<ion-fab vertical="bottom" horizontal="end" slot="fixed">
    <ion-fab-button>
        <ion-icon :icon="add"></ion-icon>
    </ion-fab-button>
</ion-fab>
</div>
</template>

<script>
import { defineComponent } from 'vue';
import { add } from "ionicons/icons";
import ConsultaDistritoSP from '../service/ConsultaDistritoSP.js';


export default defineComponent({
    name: 'MeusEnderecos',
    data(){
        return {
            add: add
        }
    },
    methods:{
        carregarCidades(){
            apiIBGE.get()
                .then((res) => mapearCidades(res.data))
                .catch((err) => console.error(err));
        },
        mapearCidades(data){
            console.log(data);
        }
    }
});

</script>

<style>
.body-layout {
    color: white;
    height: 80vh;
}

ion-card {
    text-align: left;
    border-radius: 15px;
    width: 80%;
    margin: 10px auto;
}
ion-fab{
    position: fixed;
    bottom: 10px;
    right: 5px;
}
</style>
