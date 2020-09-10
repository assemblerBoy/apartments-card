<template>
    <v-card
    max-width="500"
    class="mx-auto"
    >

    <ApartmentInfo :apartmentInfoData="data.attributes"></ApartmentInfo>
    <ApartmentAgentInfo :agentInfo="data.relationships"></ApartmentAgentInfo>

    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn icon @click="isLike = !isLike">
        <v-icon :color="isLike ? 'red' : ''">mdi-heart</v-icon>
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
import ApartmentInfo from './ApartmentInfo'
import ApartmentAgentInfo from './ApartmentAgentInfo'
export default {
    name: 'ApartmentCard',
    props:  ['data'],
    data() {
        return {
            isLike: false
        }
    },
    components: {
        ApartmentInfo, ApartmentAgentInfo
    }
}
</script>