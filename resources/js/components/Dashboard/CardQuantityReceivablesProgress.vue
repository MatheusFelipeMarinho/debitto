<template>
  <div class="card">
    <div class="card-body p-0">
      <div class="row">
        <div
          class="
            col-4
            d-flex
            align-items-center
            flex-column
            justify-content-between
            p-4
          "
        >
          <div class="mb-4">
            <span class="fa-stack fa-3x">
              <i class="fas fa-circle fa-stack-2x" style="color: #d6dce2"></i>
              <img
                class="img-fluid ml-4"
                widht="30"
                src="/images/agreement.svg"
                alt="The Logo"
                style="opacity: 0.8"
              />
            </span>
          </div>
          <div>
            <h5 class="font-weight-bold" style="color: #324e6f">R$ 0,00</h5>
          </div>
          <div class="mb-4">
            <small style="color: #324e6f">
              Acordos a receber, em andamento
            </small>
          </div>
        </div>

        <div
          class="
            col
            d-flex
            align-items-center
            flex-column
            justify-content-center
            p-4
          "
        >
          <VueApexCharts
            type="donut"
            width="350"
            height="350"
            :options="chartOptions"
            :series="series"
          />
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
      series: [10, 30, 40],
      chartOptions: {
        dataLabels: {
          enabled: false,
        },
        labels: [
          "Acordos em andamento",
          "Acordos finalizado",
          "Acordos vencidos",
        ],
        colors: ["#4CC9F0", "#0ED200", "#EB0000"],
        plotOptions: {
          pie: {
            expandOnClick: false,
          },
        },
        chart: {
          type: "donut",
        },
        responsive: [
          {
            breakpoint: 480,
            options: {
              chart: {
                width: 200,
              },
              legend: {
                position: "bottom",
              },
            },
          },
        ],
      },
    };
  },
};
</script> 

 