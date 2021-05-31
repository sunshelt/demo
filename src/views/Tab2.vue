<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 2</ion-title>
      </ion-toolbar>
    </ion-header>
      <ion-content class="ion-padding">
        <ion-list>
          <ion-item v-for="item in items" :key="item">
            <ion-label><ion-button href="view" expand="block">
              {{ item }}
            </ion-button>
            </ion-label>
          </ion-item>
        </ion-list>

        <ion-infinite-scroll
            @ionInfinite="loadData($event)"
            threshold="100px"
            id="infinite-scroll"
            :disabled="isDisabled"
        >
          <ion-infinite-scroll-content
              loading-spinner="bubbles"
              loading-text="Loading more data...">
          </ion-infinite-scroll-content>
        </ion-infinite-scroll>
      </ion-content>
    </ion-page>
</template>

<script lang="ts">
import {
  IonContent,
  IonInfiniteScroll,
  IonInfiniteScrollContent,
  IonItem,
  IonButton,
  IonList,
  IonLabel,
  IonPage
} from '@ionic/vue';
import { defineComponent, ref } from 'vue';


export default defineComponent({
  name: 'Tab2',
  components: {
    IonContent,
    IonInfiniteScroll,
    IonInfiniteScrollContent,
    IonItem,
    IonButton,
    IonList,
    IonLabel,
    IonPage,
  },
  setup() {

    // eslint-disable-next-line no-unreachable
      const isDisabled = ref(false);
      // const toggleInfiniteScroll = () => {
      //   isDisabled.value = !isDisabled.value;
      // }
    // eslint-disable-next-line no-unreachable
      const items = ref([]);
      const pushData = () => {
        const max = items.value.length + 20;
        const min = max - 20;
        for (let i = min; i < max; i++) {
          items.value.push(i);
        }
      }

    // eslint-disable-next-line no-unreachable
      const loadData = (ev: CustomEvent) => {
        setTimeout(() => {
          pushData();
          console.log('Loaded data');
          ev.target.complete();

          if (items.value.length == 1000) {
            ev.target.disabled = true;
          }
        }, 500);
      }

    // eslint-disable-next-line no-unreachable
      pushData();

      return {
        isDisabled,
        // toggleInfiniteScroll,
        loadData,
        items
      }
    }
  });

</script>
