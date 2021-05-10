<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Guessing Game</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Guessing Game</ion-title>
        </ion-toolbar>
      </ion-header>
      <Game />
      <!--<ExploreContainer name="Tab 2 page" />-->
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
//import ExploreContainer from '../components/ExploreContainer.vue';
import Game from '../components/Game.vue';


export default  {
  name: 'Tab2',
  components: { Game, IonHeader, IonToolbar, IonTitle, IonContent, IonPage }
}
</script>