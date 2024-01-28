<template>
  <ion-page>
    <ion-card>
      <ion-card-header>
        <ion-card-title>Product Page</ion-card-title>
      </ion-card-header>
      <ion-card-content>
        <ion-list>
          <ion-item v-for="(product, index) in products.data" :key="index">
            <ion-thumbnail slot="start">
              <img alt="Silhouette of mountains" src="https://ionicframework.com/docs/img/demos/thumbnail.svg" />
            </ion-thumbnail>
            <ion-label>{{product.Name}}</ion-label>
            <ion-label>{{product.Price}}</ion-label>
            <ion-label>{{product.Qty}}</ion-label>
          </ion-item>
        </ion-list>
      </ion-card-content>
    </ion-card>
  </ion-page>

</template>

<script lang="ts">
import {IonCard, IonCardContent, IonCardTitle, IonPage} from '@ionic/vue';
import {defineComponent, ref} from 'vue';
// const URL = process.env.BASE_URL_V1
const headers = { "Content-Type": "application/json" };

export default defineComponent({
  name: 'ProductList',
  components: { IonPage, IonCard, IonCardContent, IonCardTitle },
  setup(){
    const products = ref([])
      try {
        const response = fetch('http://localhost:8080/v1/products', { headers });
        response.then((res)=> {
          if(!res.ok){
              throw new Error(`HTTP error! Status: ${res.status}`);
          }
          return res.json()
        }).then((data) => {
          products.value = data
        })
      } catch (error) {
        console.error('Error fetching posts:', error);
      }

    return {products}
  }
});
</script>

<style scoped>
ion-item {
  --padding-start: 0;
}
</style>