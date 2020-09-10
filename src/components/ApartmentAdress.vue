<template>
    <v-list-item>
        <v-list-item-content>
            <v-list-item-subtitle><b>Адресс</b> - г.{{address.city}} ул.{{address.street}} д.{{address.house}} кв.{{address.room}}</v-list-item-subtitle>
        </v-list-item-content>
        
        </v-list-item>
</template>

<script>
export default {
    name: "ApartmentAdress",
    props: ['address']
    
}
</script>