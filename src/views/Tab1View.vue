<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start" mode="md">
          <ion-back-button default-href="/tabs/tab1"></ion-back-button>
        </ion-buttons>
        <ion-title>Tab 1view</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">

      <ion-button > Detail ID: {{id}}</ion-button>

    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonBackButton, IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonButton } from '@ionic/vue';
import { useRouter, useRoute } from 'vue-router';
export default  {
  name: 'tab1View',
  components: { IonBackButton,IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonButton },
  setup() {
    const route = useRoute();
    const router = useRouter();
    const { id } = route.params;
    return {  id, router };
  }


}
</script>
