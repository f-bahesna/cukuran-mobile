<template>
  <ion-page>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>
      <ion-tab-bar slot="bottom">
        <ion-tab-button tab="transaction" href="/home">
          <ion-icon aria-hidden="true" :icon="homeOutline" />
        </ion-tab-button>

        <ion-tab-button tab="product" href="/product">
          <ion-icon aria-hidden="true" :icon="listOutline" />
        </ion-tab-button>

        <ion-tab-button tab="user" href="/user">
          <ion-icon aria-hidden="true" :icon="personOutline" />
        </ion-tab-button>
      </ion-tab-bar>

    </ion-tabs>
  </ion-page>
</template>

<script setup lang="ts">
import { IonTabBar, IonTabButton, IonTabs, IonIcon, IonPage, IonRouterOutlet } from '@ionic/vue';
import { homeOutline, personOutline, listOutline } from 'ionicons/icons';
</script>
