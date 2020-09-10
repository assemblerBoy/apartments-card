<template>
    <div>
        <v-list-item>
        <v-list-item-content>
            <v-list-item-title class="headline">{{apartmentInfoData.title}}</v-list-item-title>
            <hr>
            <v-list-item-subtitle>Количество комнат: {{apartmentInfoData.rooms}}</v-list-item-subtitle>
            <v-list-item-subtitle>Метраж: {{apartmentInfoData.area + apartmentInfoData.unit}}</v-list-item-subtitle>
        </v-list-item-content>
        </v-list-item>
        <ApartmentAdress :address="apartmentInfoData.address"></ApartmentAdress>
    </div>
</template>

<script>
import ApartmentAdress from './ApartmentAdress'

export default {
    name: "ApartmentInfo",
    props: ['apartmentInfoData'],
    components: {
        ApartmentAdress
    }
}
</script>