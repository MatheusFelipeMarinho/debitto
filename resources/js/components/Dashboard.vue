<template>
  <section class="content">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-8">
          <card-receipt-information />
          <card-quantity-receivables-progress />

          <div class="row">
            <div class="col">
              <card-quantity-emails />
            </div>
            <div class="col">
              <card-quantity-debtor-interactions />
            </div>
          </div>
        </div>

        <!-- /.col -->

        <div class="col-md-4">
          <card-info-debts />
          <card-transfers />
        </div>
      </div>
      <!-- /.col -->
    </div>
  </section>
</template>

<script>
import CardQuantityEmails from "./Dashboard/CardQuantityEmails.vue";
import CardQuantityDebtorInteractions from "./Dashboard/CardQuantityDebtorInteractions.vue";
import CardQuantityReceivablesProgress from "./Dashboard/CardQuantityReceivablesProgress.vue";
import VueApexCharts from "vue-apexcharts";
import CardReceiptInformation from "./Dashboard/CardReceiptInformation.vue";
import CardInfoDebts from "./Dashboard/CardInfoDebts.vue";
import CardTransfers from "./Dashboard/CardTransfers.vue";

export default {
  components: {
    VueApexCharts,
    CardQuantityEmails,
    CardQuantityDebtorInteractions,
    CardQuantityReceivablesProgress,
    CardReceiptInformation,
    CardInfoDebts,
    CardTransfers,
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
