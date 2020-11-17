<template>
  <q-page class="">
    <div class="titulo">
      <h4>Product Backlog</h4>
    </div>
    <div class="tabla">
      <table class="content-table">
        <thead>
          <tr>
            <th>Funcionalidad</th>
            <th>Prioridad</th>
            <th>Estatus</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>FUNCIONALIDAD</td>
            <td><button class="barraAmarillo">Media</button></td>
            <td><button class="barraAmarillo">Proceso</button></td>
          </tr>
            <tr>
            <td>FUNCIONALIDAD</td>
            <td><button class="barraVerde">Baja</button></td>
            <td><button class="barraRojo">Seleccionado</button></td>
          </tr> <tr>
            <td>FUNCIONALIDAD</td>
            <td><button class="barraVerde">Baja</button></td>
            <td><button class="barraVerde">Terminado</button></td>
          </tr>
            <tr>
            <td>FUNCIONALIDAD</td>
            <td><button class="barraRojo">Alta</button></td>
            <td><button class="barraBlanco">Pendiente</button></td>
          </tr>
        </tbody>
      </table>
      <q-btn class="botonApp2 float-right" glossy label="Agregar funcionalidad" icon="add_task"/>
    </div>
  </q-page>
</template>
<script>
/* var puntoRojo = new Image()
puntoRojo.src = 'https://pbs.twimg.com/profile_images/3128936914/4c326de0f1b551ffce5c85487cf473c3.jpeg' */
import '../css/estilos.css'

export default {
  name: 'Index'
}
</script>
