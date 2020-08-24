<template>
    <v-container fluid>
        <v-layout justify-center row wrap>
            <v-flex xs10 md10 lg10 sm10>
                 <Map />
            </v-flex>
        </v-layout>
    </v-container>
</template>
<script>
import Map from '@/components/map.vue'
export default {
    components: {
       Map
    }
}
</script>