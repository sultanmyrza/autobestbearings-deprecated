<template>
  <div>
    <v-container>
      <v-row dense>
        <v-col
          v-for="card in cards"
          :key="card.title"
          :lg="cards.length > 1 ? 3 : 12"
          :md="cards.length > 1 ? 3 : 4"
          :sm="cards.length > 1 ? 3 : 6"
          :xs="cards.length > 1 ? 3 : 12"
        >
          <v-hover v-slot:default="{ hover }">
            <v-card
              :to="card.to"
              :elevation="hover ? 24 : 2"
              :ripple="false"
              append
              style="margin:8px"
            >
              <v-card-title class="headline">{{ card.title }}</v-card-title>

              <v-card-subtitle>
                <p style="height:40px">{{ card.description }}</p>
              </v-card-subtitle>

              <v-img
                :src="card.src"
                class="white--text align-end"
                :height="cards.length > 1 ? '150px' : '100%'"
              />
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  props: { cards: Array },
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped></style>
