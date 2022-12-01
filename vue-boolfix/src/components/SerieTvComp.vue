<template>
    <div class="cont-card d-flex flex-wrap py-4">
        <SerieTvCard v-for="(elem, index) in serieData" :key="index" :singleSerie="elem" />
    </div>
</template>

<script>

import SerieTvCard from './SerieTvCard.vue';

export default{
    name: 'SerieTvComp',
    props: {
        serieData: Array
    },
    components: {
        SerieTvCard
    }
}
</script>
