<template>
    <h2>Horaires d'ouverture</h2>
    <p>Du lundi au vendredi : 09h - 17h</p>
    <p>Samedi : 09h30 - 18h00</p>
    <p>Dimanche : 10h - 16h</p>
    <div v-if="reservationMode === 'reservationRequired'"><br/>Nous vous rappelons qu'il faut réserver à l'avance !</div>
</template>

<script>
import { IdentifiantMixin } from '@/Mixin.vue';

export default {
    mixins: [IdentifiantMixin],
    props: {
        reservationMode: {type: String, required: true}
    },
    created() {
        console.log(this.generateUniqueId());
    }
}
</script>
