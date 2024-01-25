<template>
  <ion-menu side="end" content-id="main-content">
    <ion-header>
      <ion-toolbar>
        <ion-title>Menu User</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      Logout
      <ion-icon name="log-out-outline"></ion-icon>
    </ion-content>
  </ion-menu>
</template>

<script lang="ts">
  import {IonMenu, IonHeader, IonIcon, IonContent} from '@ionic/vue'
  import {defineComponent} from "vue";

  export default defineComponent({
    name: 'UserPage',
    components: { IonIcon, IonMenu, IonHeader, IonContent },
  });
</script>