<template>
  <div id="app">
    <vue-plotly :data="data" :layout="layout" :options="options" />
  </div>
</template>

<script>
import VuePlotly from "@statnett/vue-plotly";

export default {
  name: "App",
  components: {
    VuePlotly
  },
  data: function() {
    return {
      data: [
        {
          values: [20700, 21800, 2300, 25200, 20100, 20800, 19600],
          labels: [
            "agent",
            "claims_ins",
            "claim_own",
            "claim_pending",
            "debt_drp",
            "debt_drp_tax",
            "debt_vet"
          ],
          domain: { column: 0 },
          name: "",
          hoverinfo: "label+percent+value",
          hole: 0.5,
          type: "pie"
        },
        {
          x: [1,2,3,4],
          y: [10,15,13,17],
          type:"scatter"
        }
      ],
      layout: {
        title: "",
        annotations: [
          {
            font: {
              size: 32
            },
            showarrow: false,
            text: "Balans",
            x: 0.5,
            y: 0.5
          }
          // {
          //   font: {
          //     size: 20
          //   },
          //   showarrow: false,
          //   text: 'CO2',
          //   x: 0.82,
          //   y: 0.5
          // }
        ],
        height: 600,
        width: 800,
        showlegend: true
      },
      options: {}
    };
  }
};
</script>

<style></style>
