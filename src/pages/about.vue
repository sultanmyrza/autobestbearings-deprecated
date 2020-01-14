<template>
  <v-layout>
    <v-flex class="text-center">
      <v-timeline :dense="$vuetify.breakpoint.smAndDown">
        <v-timeline-item color="purple lighten-2" fill-dot right>
          <v-card>
            <v-card-title class="purple lighten-2">
              <h2 class="display-1 white--text font-weight-light">
                Tier-1 Firms
              </h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col cols="12" md="10">
                  <b>Auto Industrial Co., Ltd</b> is one of main supplier for
                  international Tier one companies (Tier one companies are
                  generally the largest or the most technically-capable
                  companies in the supply chain.)
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>

        <v-timeline-item color="amber lighten-1" fill-dot left small>
          <v-card>
            <v-card-title class="amber lighten-1 justify-end">
              <h2 class="display-1 mr-4 white--text font-weight-light">
                30% of Taiwan market share
              </h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col cols="12" md="10">
                  <b>Auto Industrial Co., Ltd</b> supply 20-30% of Taiwan
                  internal market for auto accessories and constantly expanding
                  list of internetional customers.
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>

        <v-timeline-item color="cyan lighten-1" fill-dot right>
          <v-card>
            <v-card-title class="cyan lighten-1">
              <h2 class="display-1 white--text font-weight-light">
                SKF & NTN
              </h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col cols="12" md="10">
                  <b>Auto Industrial Co., Ltd</b> produces high quality products
                  suitable for the standards of companies like NTN, SKF. Also
                  producing components according to special design and customer
                  needs
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>

        <v-timeline-item color="red lighten-1" fill-dot left small>
          <v-card>
            <v-card-title class="red lighten-1 ">
              <h2 class="display-1 mr-4 white--text font-weight-light">
                1000 and more products
              </h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col cols="12" md="10">
                  <b>Auto Industrial Co., Ltd</b> Always invest in innovation
                  and development of new products. Produced more than 1000
                  products for all kinds of cars and trucks produced in Europe,
                  Japan and USA.
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>

        <v-timeline-item color="green lighten-1" fill-dot right>
          <v-card>
            <v-card-title class="green lighten-1">
              <h2 class="display-1 white--text font-weight-light">
                many years of experience
              </h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col>
                  <b>Auto Industrial Co., Ltd</b> thanks to many years of
                  experience and production capabilities the company has an
                  undeniable advantage in producing and developing new types of
                  products. <b>Auto Industrial Co., Ltd</b> have factory with
                  annual output of 100 000 - 200 000 units
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>
      </v-timeline>
      <div style="height:24px"></div>

      <v-btn :to="'contact'" x-large color="success">Contact us</v-btn>
      <div style="height:56px"></div>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        color: 'red lighten-2',
        icon: 'mdi-star'
      },
      {
        color: 'purple darken-1',
        icon: 'mdi-book-variant'
      },
      {
        color: 'green lighten-1',
        icon: 'mdi-airballoon'
      },
      {
        color: 'indigo',
        icon: 'mdi-buffer'
      }
    ]
  })
}
</script>
