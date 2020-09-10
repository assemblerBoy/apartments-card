<template>
    <v-list-item>
        <v-list-item-content>
            <v-list-item-title >Информация о продавце</v-list-item-title>
            <v-list-item-subtitle>Имя: {{ fullName() }} </v-list-item-subtitle>
        </v-list-item-content>
        </v-list-item>
</template>

<script>
export default {
    name: "ApartmentAgentInfo",
    props: ['agentInfo'],
    data() {
        return {
            fullName() {
                return this.agentInfo.attributes.last_name + ' ' + this.agentInfo.attributes.first_name + ' ' + this.agentInfo.attributes.middle_name
            }
        }
    }
}
</script>