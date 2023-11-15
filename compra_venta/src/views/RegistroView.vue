<template>
  <header class="p-3 text-bg-dark">
    <div class="container">
      <div class="d-flex flex-wrap align-items-center justify-content-center justify-content-lg-start">
        <a href="/" class="d-flex align-items-center mb-3 mb-md-0 me-md-auto link-body-emphasis text-decoration-none">
          <span class="fs-4" style="color: white">Compra & Venta</span>
        </a>
        <ul class="nav col-12 col-lg-auto me-lg-auto mb-2 justify-content-center mb-md-0">
          <li>
            <router-link to="/welcome" style="text-decoration: none">

              <a class="nav-link px-2 text-secondary rounded" style="color: white !important;border: 1px;width: 150px; height: 50px; ">Inicio</a>
            </router-link>
          </li>
        </ul>
      </div>

      <div class="text-end">
        <button type="button" class="btn btn-warning text-dark" style="background-color: grey; border-color: transparent; margin-top: -60px;border: 2px solid color: white; border;width: 150px; height: 50px;">
          <router-link to="/login" style="text-decoration: none; color: white;">
            Inicia Sesion
          </router-link>
        </button>
        
      </div>
    </div>
  </header>
  <div class="containerPrincipal">
    <div class="container mt-5">
    <div class="row justify-content-center">
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <form method="POST">
              <div class="mb-3">
                <label for="numerodoc" class="form-label">Numero De documento</label>
                <input type="text" class="form-control" id="numerodoc" name="numerodoc" required>
              </div>
              <div class="mb-3">
                <label for="contrasena" class="form-label">Contraseña</label>
                <input type="password" class="form-control" id="contrasena" name="contrasena" required>
              </div>
              <div class="mb-3">
                <label for="nombre" class="form-label">Nombre</label>
                <input type="nombre" class="form-control" id="nombre" name="nombre" required>
              </div>
              <div class="mb-3">
                <label for="apellido" class="form-label">Apellido</label>
                <input type="apellido" class="form-control" id="apellido" name="apellido" required>
              </div>
              <div class="mb-3">
                <label for="correo" class="form-label">Correo</label>
                <input type="correo" class="form-control" id="correo" name="correo" required>
              </div>
              <div class="row justify-content-center">
                <button type="submit" class="btn btn-secondary justify-content-end" style="border-color: transparent; text-primary;">
                Registrate
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
    </div>
    <div class="container mt-5">
    <footer class="d-flex flex-wrap justify-content-between align-items-center py-3 my-4 border-top">
      <p class="col-md-4 mb-0 text-body-secondary">&copy; 2023 Company, Inc</p>
      <ul class="nav col-md-4 justify-content-end">
        <li><a class="nav-link px-2 text-secondary" style="color: black !important;">¿Quienes somos?</a></li>
      </ul>
    </footer>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RegistroView'
//   props: {
//     msg: String
//   }
}
</script>

<!-- css -->
<style scoped>
header {
    padding-top: .75rem;
    padding-bottom: .75rem;
    background: linear-gradient(-60deg, #08fcfc, #212223);
    box-shadow: inset -1px 0 0 rgba(0, 0, 0, .25);
    color: white !important;
}

.containerPrincipal {
    background: linear-gradient(500deg, #c4c4c4, #828788);
    color: #000000;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    background-size: cover;
}
.nav-link
    {background: linear-gradient(500deg, #c4c4c4, #828788);}
</style>
