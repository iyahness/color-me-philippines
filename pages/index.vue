<template>
  <div class="page-container">
    <navbar></navbar>
    <div class="palette-container container">
      <div class="row">
        <div class="col palette" 
          v-for="province in provinceData.find(x => x.id === this.getProvince()).palette"
          v-bind:style="{backgroundColor: province.hex}">
          <div class="color-name">
            {{ province.name }}
          </div>
          <div class="color-hex">
            {{ province.hex }}
          </div>
        </div>
      </div>
      <div class="row province-row">
        <div class="col province-col">
          <div class="province-name">
            {{ this.getProvince() }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import navbar from '~/components/navbar'

export default {
  data() {
    return {
      currentProvince: 'Abra',
      provinceData: [
        {
          'id': 'Abra',
          'palette': [
            {
              'name': 'Midnight Blue',
              'hex': '#1C4C64',
            },
            {
              'name': 'Light Sea Green',
              'hex': '#2D9999',
            },
            {
              'name': 'Light Steel Blue',
              'hex': '#D2E2D6',
            },
            {
              'name': 'Dark Sea Green',
              'hex': '#8FB6A4',
            },
            {
              'name': 'Dark Olive Green',
              'hex': '#31662B',
            }
          ],
        }
      ]
    }
  },
  components: {
    navbar
  },
  computed: {
    selectedProvince() {
      return currentProvince;
    }
  },
  methods: {
    getProvince() {
      return 'Abra';
    }
  }
}
</script>

<style lang="scss">
.page-container {
  .palette-container {
    margin: 0;
    max-width: none;
    overflow: hidden;
    width: 100%;
    .palette {
      height: 100vh;
      text-align: center;
      .color-name, .color-hex {
        background-color: rgba($color: #000000, $alpha: 0.25);
        border-radius: 5px;
        color: white;
        margin: 12px;
        padding: 12px;
      }
    }
    .province-row {
      align-items: center;   
      display: flex;            
      flex-direction: column;   
      justify-content: center; 
      position: absolute;
      bottom: 0;
      width: 100%;
      //transform: translateY(-100%);
      .province-col {
        .province-name {
          color: rgba($color: #fff, $alpha: 0.50);
          font-family: 'Barabara';
          font-size: 100px;
          text-align: center;
        }
      }
    }
  }
}
</style>
