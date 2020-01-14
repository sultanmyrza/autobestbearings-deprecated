<template>
  <v-layout>
    <v-expansion-panels v-model="expandedPanels" :disabled="disabled" multiple>
      <v-expansion-panel>
        <v-expansion-panel-header>
          <h2>Clutch Release Bearings</h2></v-expansion-panel-header
        >
        <v-expansion-panel-content>
          <ProductsCard :cards="clutchReleaseBearings" />
        </v-expansion-panel-content>
      </v-expansion-panel>

      <v-expansion-panel>
        <v-expansion-panel-header
          ><h2>Idler Pulleys</h2></v-expansion-panel-header
        >
        <v-expansion-panel-content>
          <ProductsCard :cards="idlerPulleys" />
        </v-expansion-panel-content>
      </v-expansion-panel>

      <v-expansion-panel>
        <v-expansion-panel-header
          ><h2>Timing Belt TensionersPulleys</h2></v-expansion-panel-header
        >
        <v-expansion-panel-content>
          <ProductsCard :cards="timingBeltTensionersPulleys" />
        </v-expansion-panel-content>
      </v-expansion-panel>

      <v-expansion-panel>
        <v-expansion-panel-header
          ><h2>Automatic Belt Tensioner</h2></v-expansion-panel-header
        >
        <v-expansion-panel-content>
          <ProductsCard :cards="automaticBeltTensioner" />
        </v-expansion-panel-content>
      </v-expansion-panel>

      <v-expansion-panel>
        <v-expansion-panel-header><h2>HUB&WHEEL</h2></v-expansion-panel-header>
        <v-expansion-panel-content>
          <ProductsCard :cards="hubAndWheel" />
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </v-layout>
</template>

<script>
import ProductsCard from '../components/ProductsCard.vue'
export default {
  components: { ProductsCard },
  data() {
    // TODO: fetch procuts from real server
    const clutchReleaseBearings = this.fetchProducts('clutchReleaseBearings')
    const idlerPulleys = this.fetchProducts('idlerPulleys')
    const timingBeltTensionersPulleys = this.fetchProducts(
      'timingBeltTensionersPulleys'
    )
    const automaticBeltTensioner = this.fetchProducts('automaticBeltTensioner')
    const hubAndWheel = this.fetchProducts('hubAndWheel')

    return {
      expandedPanels: [0, 1, 2, 3, 4],
      disabled: false,
      readonly: false,
      clutchReleaseBearings,
      idlerPulleys,
      timingBeltTensionersPulleys,
      automaticBeltTensioner,
      hubAndWheel
    }
  },
  methods: {
    fetchProducts(category) {
      const clutchReleaseBearings = [
        {
          src: 'http://autobestbearings.com/images/prodructs/01/1.jpg',
          title: 'prodructs-01-1',
          description: 'prodructs-01-1',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/01/2.jpg',
          title: 'prodructs-01-2',
          description: 'prodructs-01-2',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/01/3.jpg',
          title: 'prodructs-01-3',
          description: 'prodructs-01-3',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/01/4.jpg',
          title: 'prodructs-01-4',
          description: 'prodructs-01-4',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/01/5.jpg',
          title: 'prodructs-01-5',
          description: 'prodructs-01-5',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/01/6.jpg',
          title: 'prodructs-01-6',
          description: 'prodructs-01-6',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/01/7.jpg',
          title: 'prodructs-01-7',
          description: 'prodructs-01-7',
          to: ''
        }
      ]

      const idlerPulleys = [
        {
          src: 'http://autobestbearings.com/images/prodructs/02/1.jpg',
          title: 'prodructs-02-1',
          description: 'prodructs-02-1',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/02/2.jpg',
          title: 'prodructs-02-2',
          description: 'prodructs-02-2',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/02/3.jpg',
          title: 'prodructs-02-3',
          description: 'prodructs-02-3',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/02/4.jpg',
          title: 'prodructs-02-4',
          description: 'prodructs-02-4',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/02/5.jpg',
          title: 'prodructs-02-5',
          description: 'prodructs-02-5',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/02/6.jpg',
          title: 'prodructs-02-6',
          description: 'prodructs-02-6',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/02/7.jpg',
          title: 'prodructs-02-7',
          description: 'prodructs-02-7',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/02/8.jpg',
          title: 'prodructs-02-8',
          description: 'prodructs-02-8',
          to: ''
        }
      ]

      const timingBeltTensionersPulleys = [
        {
          src: 'http://autobestbearings.com/images/prodructs/03/1.jpg',
          title: 'prodructs-03-1',
          description: 'prodructs-03-1',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/03/2.jpg',
          title: 'prodructs-03-2',
          description: 'prodructs-03-2',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/03/3.jpg',
          title: 'prodructs-03-3',
          description: 'prodructs-03-3',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/03/4.jpg',
          title: 'prodructs-03-4',
          description: 'prodructs-03-4',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/03/5.jpg',
          title: 'prodructs-03-5',
          description: 'prodructs-03-5',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/03/6.jpg',
          title: 'prodructs-03-6',
          description: 'prodructs-03-6',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/03/7.jpg',
          title: 'prodructs-03-7',
          description: 'prodructs-03-7',
          to: ''
        },
        {
          src: 'http://autobestbearings.com/images/prodructs/03/8.jpg',
          title: 'prodructs-03-8',
          description: 'prodructs-03-8',
          to: ''
        }
      ]

      const automaticBeltTensioner = [
        {
          src: 'http://autobestbearings.com/images/prodructs/auto.jpg',
          title: 'images-prodructs-auto',
          description: 'images-prodructs-auto',
          to: ''
        }
      ]

      const hubAndWheel = [
        {
          src: 'http://autobestbearings.com/images/prodructs/hub.jpg',
          title: 'images-prodructs-hub',
          description: 'images-prodructs-hub',
          to: ''
        }
      ]

      const result = {
        clutchReleaseBearings,
        idlerPulleys,
        timingBeltTensionersPulleys,
        automaticBeltTensioner,
        hubAndWheel
      }[category]
      return result
    }
  }
}
</script>

<style></style>
