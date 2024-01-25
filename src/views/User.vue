<template>
  <ion-page id="main-content">
    <ion-menu side="end" content-id="main-content">
      <ion-header>
        <ion-toolbar>
          <ion-title>Nama User</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content class="ion-padding">
        <ion-button color="danger">Logout</ion-button>
        <ion-icon name="log-out-outline"></ion-icon>
      </ion-content>
    </ion-menu>
    <ion-header>
      <ion-toolbar>
        <ion-title>User</ion-title>
        <ion-buttons slot="end">
          <ion-menu-button></ion-menu-button>
        </ion-buttons>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding"> Nama : <br> Toko : </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonButtons, IonContent, IonHeader, IonMenu, IonMenuButton, IonPage, IonTitle, IonToolbar, IonIcon } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: "MainMenu",
  components: {
    IonButtons,
    IonContent,
    IonHeader,
    IonMenu,
    IonMenuButton,
    IonPage,
    IonTitle,
    IonToolbar,
    IonIcon
  },
});
</script>