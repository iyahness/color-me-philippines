<template>
  <div class="sidebarContainer">
    <div class="province" v-for="province in provinces" @click="$emit('province-selected', province)">
      {{ province }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      provinces: ["Abra", "Agusan del Norte", "Agusan del Sur", "Aklan", "Albay", "Angeles", "Antique", "Apayao", "Aurora", "Baguio", "Basilan", "Bataan", "Batanes", "Batangas", "Benguet", "Biliran", "Bohol", "Bukidnon", "Bulacan", "Cagayan", "Camarines Norte", "Camarines Sur", "Camiguin", "Capiz", "Catanduanes", "Cavite", "Cebu", "Compostela Valley", "Cotabato", "Dagupan", "Davao Occidental", "Davao Oriental", "Davao del Norte", "Davao del Sur", "Dinagat Islands", "Eastern Samar", "Guimaras", "Ifugao", "Ilocos Norte", "Ilocos Sur", "Iloilo", "Isabela", "Kalinga", "La Union", "Laguna", "Lanao del Norte", "Lanao del Sur", "Leyte", "Lucena", "Maguindanao", "Marinduque", "Masbate", "Metro Manila", "Mindoro Occidental", "Mindoro Oriental", "Misamis Occidental", "Misamis Oriental", "Mountain Province", "Naga", "Negros Occidental", "Negros Oriental", "Northern Samar", "Nueva Ecija", "Nueva Vizcaya", "Olongapo", "Palawan", "Pampanga", "Pangasinan", "Puerto Princesa", "Quezon", "Quirino", "Rizal", "Romblon", "Samar", "Santiago", "Sarangani", "Siquijor", "Sorsogon", "South Cotabato", "Southern Leyte", "Sultan Kudarat", "Sulu", "Surigao del Norte", "Surigao del Sur", "Tarlac", "Tawi-Tawi", "Zambales", "Zamboanga", "Zamboanga del Norte", "Zamboanga del Sur"]
    }
  }
}
</script>

<style lang="scss" scoped>
.sidebarContainer {
  // background: rgb(55,55,55);
  // background: linear-gradient(180deg, rgba(55,55,55,1) 0%, rgba(11,11,11,1) 100%);
  background-color: rgba($color: #000000, $alpha: 0.25);
  color: white;
  height: 100vh;
  overflow-y: scroll;
  position: fixed;
  // width: 200px;
  .province {
    &:hover {
      // transform: scale(1.5);
      // transform-origin: center left;
    }
    padding: 5px 12px;
    transition: 0.25s;
  }
}
</style>
