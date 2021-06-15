<template>
  <section class="content">
    <div class="container-fluid">
      <div class="row mb-2">
        <div class="col-md-12">
          <div
            class="row d-flex align-items-center justify-content-between p-1"
          >
            <div class="col-6">
              <h3 class="font-weight-bold" style="color: #324e6f">
                Meus devedores
              </h3>
            </div>
            <div class="col-3">
              <input
                type="text"
                size="4"
                class="form-control form-rounded"
                placeholder="Buscar aqui..."
              />
            </div>
            <div class="col-2">
              <button
                type="button"
                class="btn btn-primary"
                data-toggle="button"
                aria-pressed="false"
                autocomplete="off"
              >
                Adicionar
              </button>
            </div>
          </div>

          <div class="card mt-2">
            <div class="card-body">
              <table class="table">
                <thead>
                  <tr>
                    <th>Nome</th>
                    <th>CPF/CNPJ</th>
                    <th>Atraso</th>
                    <th>Valor da divida</th>
                    <th class="border-right-0">Status</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="row in debtors" :key="row.id">
                    <td>{{ row.name }}</td>
                    <td>{{ row.document }}</td>
                    <td>{{ row.atraso }}</td>
                    <td>{{ row.value }}</td>
                    <td class="border-right-0">{{ row.status }}</td>
                    <!-- <td><img v-bind:src="'/' + product.photo" width="100" alt="product"></td> -->
                  </tr>
                </tbody>
              </table>
            </div>
            <!-- /.card-body -->
            <!-- <div class="card-footer">
              <pagination :data="debtors"></pagination>
            </div> -->
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      debtors: [
        {
          id: 1,
          name: "Jorge Elias",
          document: "000.000.000-00",
          atraso: "60 dias",
          value: "10",
          status: "pendente",
        },
        {
          id: 2,
          name: "Jorge Elias",
          document: "000.000.000-00",
          atraso: "60 dias",
          value: "10",
          status: "pendente",
        },
        {
          id: 3,
          name: "Jorge Elias",
          document: "000.000.000-00",
          atraso: "60 dias",
          value: "10",
          status: "pendente",
        },
        {
          id: 4,
          name: "Jorge Elias",
          document: "000.000.000-00",
          atraso: "60 dias",
          value: "10",
          status: "pendente",
        },
        {
          id: 5,
          name: "Jorge Elias",
          document: "000.000.000-00",
          atraso: "60 dias",
          value: "10",
          status: "pendente",
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
  width: 200px;
  font-size: 16px;
  color: #fff;
  line-height: 25px;
  border: none;
  border-radius: 40px;
  background: #324e6f;
  transition: all 0.3s ease 0s;
}
.form-rounded {
  border-radius: 1rem;
}

table th {
  border-right: 1px solid rgb(170, 170, 170);
   text-align: center;
}

table td {
  border-top: none;
  text-align: center;
  border-right: 1px solid rgb(170, 170, 170);
}
</style>
