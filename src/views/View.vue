<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start" mode="md">
          <ion-back-button default-href="/tabs/tab1"></ion-back-button>
        </ion-buttons>
        <ion-title> view</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">

      <ion-button router-link="/tabs/tab1">  Back </ion-button>

    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonBackButton, IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonButton } from '@ionic/vue';
import { useRouter } from 'vue-router';
export default  {
  name: 'View',
  components: { IonBackButton, IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonButton },
  setup() {
    const router = useRouter();
    return { router };
  }
}
</script>
