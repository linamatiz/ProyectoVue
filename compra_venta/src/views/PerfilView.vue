<template>
    <header class="p-3 text-bg-dark">
        <div class="container">
            <div class="d-flex flex-wrap align-items-center justify-content-center justify-content-lg-start">
                <a href="/" class="d-flex align-items-center mb-1 mb-md-0 me-md-auto link-body-emphasis text-decoration-none">
                    <span class="fs-4" style="color: white">Compra & Venta</span>
                        </a>
            </div>
        </div>
            
    </header>

    <div class="container">
 
        <!-- actualizacion de datos">
        
        </div> -->
        <div class="col-md-8">
            <div class="card">
                <div class="card-header">Actualizar Perfil</div>
                    <div class="card-body">
                        <form method="POST">
                            <div class="form-group">
                                <label for="numero_documento">Número de Documento</label>
                                <input type="text" class="form-control" id="numero_documento" name="numero_documento"  disabled>
                            </div>
                            <div class="form-group">
                                <label for="nombre">Nombre</label>
                                <input type="text" class="form-control" id="nombre" name="nombre" >
                            </div>
                            <div class="form-group">
                                <label for="apellido">Apellido</label>
                                <input type="text" class="form-control" id="apellido" name="apellido">
                            </div>
                            <div class="form-group">
                                <label for="correo">Correo</label>
                                <input type="text" class="form-control" id="correo" name="correo" >
                            </div>
                            <div class="form-group">
                                <label for="password">Contraseña</label>
                                <input type="password" class="form-control" id="password" name="password" >
                            </div>
                            <button type="submit" class="btn btn-primary">Actualizar Perfil</button>
                        </form>
                            <button class="btn btn-danger me-2">Atras</button>
                    </div>
                </div>
        </div>
    </div>
    <div class="container mt-5">
        <footer class="d-flex flex-wrap justify-content-between align-items-center py-3 my-4 border-top">
            <p class="col-md-4 mb-0 text-body-secondary">&copy; 2023 Company, Inc</p>
                <ul class="nav col-md-4 justify-content-end">
                    <li>
                    <a class="nav-link px-2 text-secondary" style="color: black !important;">&copy; 2023 Company, Inc</a>
                </li>
            </ul>
        </footer>
    </div>
</template>

<script>
export default {
  name: 'PerfilView'
//   props: {
//     msg: String
//   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
