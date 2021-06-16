<template>
  <div>
    <div class="pb-2">
      <h4 class="font-weight-bold" style="color: #324e6f">Dívidas</h4>
    </div>
    <div class="info-box mb-3">
      <span class="info-box-icon mr-0"><span class="dot"></span></span>

      <div class="d-flex flex-row align-items-center justify-content-around">
        <div class="pr-5 mr-5">
          <span class="text-left font-weight-bold" style="color: #324e6f"
            >Pendentes</span
          >
        </div>
        <div class="text-right pl-5 ml-5">
          <span class="text-left font-weight-bold" style="color: #324e6f"
            >2 dividas</span
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VueApexCharts from "vue-apexcharts";

export default {
  components: {
    VueApexCharts,
  },
  data() {
    return {
      options: {
        chart: {
          id: "vuechart-example",
          zoom: {
            enabled: false,
          },
        },
        markers: {
          size: [5],
        },
        grid: {
          row: {
            colors: ["#f3f3f3", "transparent"], // takes an array which will be repeated on columns
            opacity: 0.5,
          },
        },
        xaxis: {
          categories: [
            "jan",
            "fev",
            "mar",
            "abr",
            "mai",
            "jun",
            "jul",
            "ago",
            "set",
            "out",
            "nov",
            "dez",
          ],
        },
      },
      series: [
        {
          name: "series-1",
          data: [5, 40, 45, 49, 30, 45, 50, 35, 40, 45, 50, 49],
        },
      ],
    };
  },
  mounted() {
    console.log("Component mounted.");
  },
};
</script>
<style scoped>
.dot {
  height: 12px;
  width: 12px;
  background-color: #324e6f;
  border-radius: 50%;
  display: inline-block;
}
.btn-primary {
  margin-top: 12px;
  font-size: 16px;
  color: #fff;
  line-height: 25px;
  border: none;
  border-radius: 40px;
  background: #324e6f;
  transition: all 0.3s ease 0s;
}
</style>
