<template>
  <div style="height: 95vh">
    <chart
      :data="jsonData"
      :labels="labels"
      :options="options"
      :fillAlpha="0.3"
    />
  </div>
</template>

<script>
import jsonData from "./data.json";
//import jsonData from "./data_2022.json";
import Chart from "./components/Chart.vue";
import jsonData_2022 from "./data_2022.json";

/// display jsonData & jsonData_2022
console.log("BEGIN");
console.log(jsonData);
console.log(jsonData_2022);

export default {
  name: "app",
  components: {
    Chart,
  },
  data() {
    return {
      jsonData,
      labels: ["Label 1", "Label 2"],
      options: {
        maintainAspectRatio: false,
      },
    };
  },
};
</script>
