<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Bye Bye</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Bye Bye</ion-title>
        </ion-toolbar>
      </ion-header>
      <h3 style="color: limegreen; text-align: center; margin-top: 200px; font-weight: bold">THANKS FOR PLAYING!!</h3>
      <img style="height: 200px; margin: auto; display: block" src="../images/byebye.jpg">
      <ion-button id="container" style="width: 200px; display: block; margin: auto" href="/tabs/tab1">Return Home</ion-button>
      <!--<ExploreContainer name="Tab 3 page" />-->
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
//import ExploreContainer from '../components/ExploreContainer.vue';

export default  {
  name: 'Tab3',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage }
}
</script>