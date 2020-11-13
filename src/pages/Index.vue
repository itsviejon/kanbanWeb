<template>
  <q-page class="">
    <div class="titulo">
      <h3>Tablero Kanban</h3>
    </div>
    <div class="tabla">
      <table class="content-table">
        <thead>
          <tr>
            <th>Nombre</th>
            <th>Prioridad</th>
            <th>Estatus</th>
            <th>Fecha Estatus</th>
            <th>Development</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>SIAN</td>
            <td></td>
            <td></td>
            <td>10/15/2020</td>
            <td>Fernando Arteaga</td>
          </tr>
           <tr>
            <td>SACEC</td>
            <td></td>
            <td></td>
            <td>08/05/2020</td>
            <td>José López</td>
          </tr>
           <tr>
            <td>EBIND</td>
            <td></td>
            <td></td>
            <td>10/27/2020</td>
            <td>Pedro Fuentes</td>
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
