<template>
  <v-card
    elevation="3"
    class="mx-auto my-12 mt-16"
    max-width="550"
    outlined
  >
    <v-sheet
        class="v-sheet--offset mx-auto"
        color="grey"
        elevation="12"
        max-width="calc(100% - 32px)"
    >
      <v-sparkline
        :labels="labels"
        :value="value"
        color="white"
        line-width="2"
        padding="16"
      ></v-sparkline>
    </v-sheet>

    <v-card-text class="pt-0">
      <div class="text-h3 font-weight-light mb-2">
        Histórico
      </div>
      <div class="subheading font-weight-light grey--text">
        Utilização de créditos nos últimos 7 dias
      </div>
    </v-card-text>
  </v-card>
</template>


<script>
  export default {
    data: () => ({
      labels: [
        '24/06',
        '25/06',
        '26/06',
        '27/06',
        '28/06',
        '29/06',
        '30/06',
      ],
      value: [
        200,
        675,
        410,
        390,
        310,
        460,
        240,
      ],
    }),
  }
</script>

<style>
  .v-sheet--offset {
    top: -24px;
    position: relative;
  }
</style>