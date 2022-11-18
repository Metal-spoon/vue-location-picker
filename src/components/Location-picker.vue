<script setup lang="ts">
    import * as L from 'leaflet'
import { onMounted } from 'vue';

    
    onMounted(() => {
        var map = L.map('map').setView([51.505, -0.09], 13);
        L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
        }).addTo(map);
    })
</script>

<template>
    <div id="map"></div>
</template>

<style scoped>
    #map {
        height: 500px;
        width: 500px;
    }
</style>