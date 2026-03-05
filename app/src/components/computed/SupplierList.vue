<script setup>
import { ref, computed } from "vue"

const props = defineProps({
  fullName: {
    type: String,
    required: true
  },
  totalPrice: {
    type: String,
    required: true
  }
})

const search = ref("")
const supplyers = ref([
  { fullName: "Sergiu Firulescu", totalPrice: "20.22 $" },
  { fullName: "Elisei Morosan", totalPrice: "36.51 $" }
])

const filteredSupplyers = computed(() =>
  supplyers.value.filter(s => s.fullName.toLowerCase().includes(search.value.toLowerCase()))
)

const addToList = () => {
  supplyers.value.push({
    fullName: props.fullName,
    totalPrice: props.totalPrice
  })
}
</script>

<template>
  <input class="border" v-model="search" placeholder="Search" />

  <button
    type="button"
    class="ml-4 cursor-pointer rounded bg-blue-500 px-4 py-2 text-white"
    @click="addToList"
  >
    Add to list of suppliers
  </button>
  <hr class="my-4" />

  <ul>
    <li v-for="(supplyer, i) in filteredSupplyers" :key="i">
      {{ supplyer.fullName }} > {{ supplyer.totalPrice }}
    </li>
  </ul>
</template>
