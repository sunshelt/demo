<template>
  <ion-app>
    <ion-router-outlet />
  </ion-app>
</template>

<script lang="ts">

import { IonApp, IonRouterOutlet } from '@ionic/vue';
import { defineComponent } from 'vue';
// import { useIonRouter } from '@ionic/vue';

export default defineComponent({
  name: 'App',
  components: {
    IonApp,
    IonRouterOutlet
  },
  // setup() {
  //   const ionRouter = useIonRouter();
  //   if (ionRouter.canGoBack()) {
  //     // Perform some action here
  //   }
  // }
});
</script>
