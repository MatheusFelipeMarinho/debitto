
<template>
  <nav class="navbar navbar-expand-lg">
    <a class="ml-3 navbar-brand" href="#"
      ><img
        src="http://localhost:8000/images/logo.svg"
        alt="The Logo"
        style="opacity: 0.8"
    /></a>

    <div class="collapse navbar-collapse" id="conteudoNavbarSuportado">
      <ul class="navbar-nav ml-auto">
        <li class="nav-item active">
          <a class="nav-link" href="#">
            <span class="sr-only">(página atual)</span></a
          >
        </li>

        <ul class="navbar-nav align-items-center ml-auto ml-md-0">
          <li class="nav-item">
            <a
              class="nav-link pr-0 mr-0"
              href="#"
              role="button"
              aria-haspopup="true"
              aria-expanded="false"
            >
              <div class="media align-items-center">
                <div class="media-body text-right mr-2 d-none d-lg-block">
                  <span class="mb-0 text-sm font-weight-bold"
                    >Lucas Estevam</span
                  >
                  <br />
                  <span style="font-size: 10px" class="mb-0"
                    >Administrador</span
                  >
                </div>
                <span class="avatar avatar-sm rounded-circle">
                  <img
                    src="https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/13-small.d796bffd.png"
                    width="50"
                    height="50"
                    class="rounded-circle"
                  />
                </span>
              </div>
            </a>
          </li>
          <li class="nav-item mr-2">
            <a
              @click="logout()"
              class="nav-link ml-0 pr-0"
              href="#"
              role="button"
              aria-haspopup="true"
              aria-expanded="false"
            >
              <div class="media align-items-center">
                <div class="media-body ml-2 d-none d-lg-block">
                  <span class="mb-0 text-sm font-weight-bold">Sair</span>
                </div>
              </div>
            </a>
          </li>
        </ul>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    logout() {
      console.log("logout");
    },
  },
};
</script>

<style>
</style>