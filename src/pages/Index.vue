<template>
  <q-page class="">
    <div class="tabla">
      <table class="content-table">
        <thead>
          <tr>
            <th>#</th>
            <th>Funcionalidad</th>
            <th>Prioridad</th>
            <th>Estatus</th>
            <th>Fecha Estatus</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>Funcionalidad</td>
            <td><button class="circuloRojo"></button></td>
            <td><button class="circuloVerde"></button></td>
            <td>10/15/2020</td>
          </tr>
           <tr>
            <td>2</td>
            <td>Funcionalidad</td>
            <td><button class="circuloRojo"></button></td>
            <td><button class="circuloAmarillo"></button></td>
            <td>08/05/2020</td>
          </tr>
           <tr>
            <td>3</td>
            <td>Funcionalidad</td>
            <td><button class="circuloAmarillo"></button></td>
            <td><button class="circuloBlanco"></button></td>
            <td>10/27/2020</td>
          </tr>
        </tbody>
      </table>
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
