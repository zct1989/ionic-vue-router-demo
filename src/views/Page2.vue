<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot:start>
          <ion-back-button></ion-back-button>
        </ion-buttons>
        <ion-title>Page2</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      Page ,Try To Client Left Top Back Button
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
} from "@ionic/vue";
import { useRouter } from "vue-router";

export default {
  name: "Tab1",
  components: {
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage,
  },
  setup() {
    const redirect = () => {
      const router = useRouter();
      router.push({ name: "page2" });
    };

    return {
      redirect,
    };
  },
};
</script>
