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
              <i class="fas fa-circle fa-stack-2x" style="color: #d8efea"></i>
              <img
                class="img-fluid ml-4"
                widht="30"
                src="/images/money.png"
                alt="The Logo"
                style="opacity: 0.8"
              />
            </span>
          </div>
          <div>
            <h5 class="font-weight-bold" style="color: #324e6f">R$ 0,00</h5>
          </div>
          <div class="mb-4">
            <small style="color: #324e6f"> Total recuperado no período </small>
          </div>
          <div>
            <h5 class="font-weight-bold" style="color: #324e6f mb-0">
              R$ 0,00
            </h5>
          </div>
          <div class="mb-2">
            <small style="color: #324e6f">
              Total de pagamentos do período</small
            >
          </div>
        </div>
        <div
          class="
            col-md-8
            d-flex
            align-items-center
            flex-column
            justify-content-between
            p-4
          "
        >
          <!-- <div class="mb-2">skadlkl</div> -->
          <VueApexCharts
            width="530"
            height="200"
            type="line"
            :options="options"
            :series="series"
          ></VueApexCharts>
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
