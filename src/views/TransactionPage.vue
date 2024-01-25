<template>
  <ion-page>
    <ion-card>
      <ion-card-header>
        <ion-card-title>Transaction Page</ion-card-title>
      </ion-card-header>
      <ion-card-content>
        <ion-list>
          <ion-item>
            <ion-thumbnail slot="start">
              <img alt="Silhouette of mountains" src="https://ionicframework.com/docs/img/demos/thumbnail.svg" />
            </ion-thumbnail>
            <ion-label>Item</ion-label>
          </ion-item>

          <ion-item>
            <ion-thumbnail slot="start">
              <img alt="Silhouette of mountains" src="https://ionicframework.com/docs/img/demos/thumbnail.svg" />
            </ion-thumbnail>
            <ion-label>Item</ion-label>
          </ion-item>

          <ion-item>
            <ion-thumbnail slot="start">
              <img alt="Silhouette of mountains" src="https://ionicframework.com/docs/img/demos/thumbnail.svg" />
            </ion-thumbnail>
            <ion-label>Item</ion-label>
          </ion-item>

          <ion-item lines="none">
            <ion-thumbnail slot="start">
              <img alt="Silhouette of mountains" src="https://ionicframework.com/docs/img/demos/thumbnail.svg" />
            </ion-thumbnail>
            <ion-label>Item</ion-label>
          </ion-item>
        </ion-list>
      </ion-card-content>
    </ion-card>
  </ion-page>
</template>

<script lang="ts">
import { IonCard, IonCardContent, IonCardHeader, IonCardTitle, IonPage } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'TransactionPage',
  components: { IonCard, IonCardContent, IonCardHeader, IonCardTitle, IonPage },
});
</script>

<style scoped>
ion-item {
  --padding-start: 0;
}
</style>