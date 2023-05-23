<template>
 <div class="results-country" v-if="country">{{country}}</div>
 <div class="results-city" v-if="cityName">{{ cityName }}</div>
 <div class="results-temp" v-if="temperature">{{ temperature }}</div>
 <div v-if="icon"><img :src="icon" alt="icon">
    <span>{{conditionText }}</span>
 </div>
 <div class="loading"></div>
</template>

<script setup>
import {toRefs} from "vue"
const props = defineProps({
    results:Object
})

const {
    country,
    cityName,
    temperature,
    icon,
    conditionText} =toRefs(props.results)
</script>
