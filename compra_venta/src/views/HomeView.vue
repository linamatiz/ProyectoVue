<template>
  <header class="p-3 text-bg-dark">
       <div class="container">
           <div class="d-flex flex-wrap align-items-center justify-content-center justify-content-lg-start">
               <a href="/" class="d-flex align-items-center mb-3 mb-md-0 me-md-auto link-body-emphasis text-decoration-none">
                   <span class="fs-4" style="color: white">Compra & Venta</span>
               </a>
               <ul class="nav col-12 col-lg-auto me-lg-auto mb-2 justify-content-center mb-md-0">
                   <li><a class="nav-link px-2 text-secondary" style="color: white !important;">¿Quienes somos?</a></li>
               </ul>

               <div class="text-end mr-5">
                   <button type="button" class="btn btn-danger me-2">
                       <a style="text-decoration: none !important;">Cierra Sesion</a>
                   </button>
                   <button type="button" class="btn btn-danger me-2" style="background-color: darkslategray; border-color:black">
                       <a style="text-decoration: none !important; color: white;">Perfil</a>
                       <i class="fas fa-user-circle" style="font-size: 25px"></i>
                   </button>
               </div>
           </div>
       </div>
   </header>

   <div class="container-fluid">
       <div class="row m-3">
           <div class="col-md-9">
               <div class="container">
                   <div class="row scrollable-content">
                   <div class="col-4 mt-2" v-for="producto in productos" :key="producto">
                        <div class="card" style="width: 18rem;">
                           <img class="card-img-top" loading="lazy" src="@/assets/pngwing.png" alt="Imagen de Bienvenida">
                           <div class="card-body">
                               <h5 class="card-title">{{ producto.titulo }}</h5>
                               <p class="card-text">{{ producto.descrip }}</p>
                               <p class="card-text">{{ producto.precio }}</p>
                               <button type="button"  @click="showData(producto)" class="btn btn-primary">Añadir al Carrito</button>
                           </div>
                       </div>
                   </div>
               </div>
               </div>
           </div>
           <div class="col-md-3 carrito scrollable-content" style="border">
               <div>Carrito de compras</div>
               <div class="card" style="width: 18rem;">
                 <div class="card-body">
                     <div class="row">
                       <div class="col">
                         <ul v-for="producto in prodoctoLista" :key="producto">
                           <li>{{producto.titulo}} = {{ producto.precio }}</li>
                         </ul>
                       </div>
                     </div>  

                     <p class="card-text"><strong>Total:</strong> {{ totalCarrito }}</p>
                     <button type="button" class="btn btn-primary mt-2">Comprar</button><br>
                     <button type="button" class="btn btn-danger mt-3" @click="clearData">Limpiar carrito</button>
                 </div>
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
 name: 'HomeView',
//   props: {
//     
//   }
   data() {
   return {
     prodoctoLista: [],
     totalCarrito: 0,
     totales: [],
     productos: [
       { id: 1, titulo: 'motorola one fusion', precio: 1000.000, descrip: 'gb 68 , ram 4'},
       { id: 2, titulo: 'samsung galaxy s4 ', precio: 1500.000, descrip: 'bonito'},
       { id: 3, titulo: 'iphone 8 plus', precio: 2000.000, descrip: 'bonito'},
       { id: 4, titulo: 'iphone x ', precio: 2500.000, descrip: 'bonito'},
       { id: 5, titulo: 'Samsung m12', precio: 2500.000, descrip: 'bonito'},
       { id: 6, titulo: 'motorola e 32 ', precio: 2500.000, descrip: 'bonito'},
       { id: 7, titulo: 'Samsung galaxy s3 ultra +', precio: 2500.000, descrip: 'bonito'},
       { id: 8, titulo: 'iphone 14 pro max +', precio: 2500.000, descrip: 'bonito'},
       { id: 9, titulo: 'iphone 7 plus', precio: 500.000, descrip: 'bonito'},
     ]
   }
 },
 methods: {
   showData(precio){
    
     this.totales.push(precio.precio);
     this.prodoctoLista.push(precio)

     this.totalCarrito = this.totales.reduce((total, valor) => total + valor, 0);
       
     console.log("suma", this.totalCarrito);
   },

   clearData() {
     this.totales = [...[]]
     this.prodoctoLista = [...[]]
     this.totalCarrito = 0
   }
 },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
   padding-top: .75rem;
   padding-bottom: .75rem;
   background: linear-gradient(70deg, #08fcfc, #212223);
   box-shadow: inset -1px 0 0 rgba(0, 0, 0, .25);
   color: white !important;
}
.card {
   border-color: #08fcfc;
}
.carrito {
   border: 1px solid;
   border-bottom-color: transparent;
   border-right-color: transparent;
   border-top-color: transparent;
   border-left-color: linear-gradient(70deg, #08fcfc, #212223);
}

.scrollable-content {
 max-height: 400px;
 overflow-y: auto;
}
.scrollable-content::-webkit-scrollbar {
 width: 12px; /* Ancho de la barra de desplazamiento */
}

/* Estilo del pulgar de la barra de desplazamiento */
.scrollable-content::-webkit-scrollbar-thumb {
 background-color: #08fcfc; /* Color de fondo del pulgar */
 border-radius: 6px; /* Borde redondeado del pulgar */
 border-color: #828788;
}

/* Estilo de la pista de la barra de desplazamiento */
.scrollable-content::-webkit-scrollbar-track {
 background-color: #f1f1f1; /* Color de fondo de la pista */
}
</style>
