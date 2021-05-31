<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <div class="ion-padding" style="margin-top: 2.6rem;overflow: scroll;padding-bottom: 3rem;">
        <ion-item lines="none">
          <ion-avatar slot="end">
            <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
          </ion-avatar>
          <ion-label>
            <h2>loginName</h2>
          </ion-label>
        </ion-item>

        <!-- Some Menu Options -->
        <ion-card mode="ios">
          <ion-grid>
            <ion-row class="ion-text-center">
              <ion-col>
                <ion-icon name="heart" style="zoom:1.5;"></ion-icon>
                <br/>
                <ion-text>我的愿望清单</ion-text>
              </ion-col>
              <ion-col>
                <ion-icon name="checkbox-outline" style="zoom:1.5;"></ion-icon>
                <br/>
                我的订单
              </ion-col>

              <ion-col>
                <ion-icon name="images" style="zoom:1.5;"></ion-icon>
                <br/>
                images
              </ion-col>
            </ion-row>
          </ion-grid>
        </ion-card>
        <ion-card mode="ios">
          <ion-item-group>
            <ion-item lines="none">
              <ion-label>lines1</ion-label>
              <ion-icon slot="end" mode="ios" name="arrow-forward" size="small"></ion-icon>
            </ion-item>
            <ion-item lines="none">
              <ion-label>lines2</ion-label>
              <ion-icon slot="end" mode="ios" name="arrow-forward" size="small"></ion-icon>
            </ion-item>
            <ion-item lines="none">
              <ion-label>lines3</ion-label>
              <ion-icon slot="end" mode="ios" name="arrow-forward" size="small"></ion-icon>
            </ion-item>
            <ion-item lines="none">
              <ion-label>lines4</ion-label>
              <ion-icon slot="end" mode="ios" name="arrow-forward" size="small"></ion-icon>
            </ion-item>
            <ion-item lines="none">
              <ion-label>lines5</ion-label>
              <ion-icon slot="end" mode="ios" name="arrow-forward" size="small"></ion-icon>
            </ion-item>

          </ion-item-group>
        </ion-card>
      </div>
    </ion-content>

  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonContent } from '@ionic/vue';


export default  {
  name: 'Tab3',
  components: { IonContent, IonPage }
}
</script>
