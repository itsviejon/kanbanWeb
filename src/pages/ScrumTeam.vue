<template>
  <div class="q-pa-md" style="margin-left:10%; margin-right:10%; ">
   <div class="titulo">
      <h4>Scrum Team</h4>
    </div>
    <div class="tabla">
      <table class="content-table">
        <thead>
          <tr>
            <th>#</th>
            <th>NAA</th>
            <th>Clave</th>
            <th>Primer Apellido</th>
            <th>Segundo Apellido</th>
          </tr>
        </thead>
        <tbody>
           <tr>
            <td>1</td>
            <td>Fernando</td>
            <td>Arteaga</td>
            <td>Cortez</td>
            <td>Rol</td>
          </tr>
        </tbody>
      </table>
    </div>
    <a href="#/formScrum">
        <q-btn class="botonApp" glossy label="Agregar" icon="people"  />
    </a>
  </div>
</template>

<script>
import '../css/estilos.css'

export default {
  name: 'PageIndex'
}
</script>
