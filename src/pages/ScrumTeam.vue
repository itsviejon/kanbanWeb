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
            <th>Clave</th>
            <th>Nombre</th>
            <th>Primer Apellido</th>
            <th>Segundo Apellido</th>
            <th>Product owner</th>
          </tr>
        </thead>
        <tbody>
           <tr>
            <td>numero</td>
            <td>Clave</td>
            <td>Nombre</td>
            <td>Apellido</td>
            <td>Apellido</td>
                        <td>Ownner</td>
          </tr>
        </tbody>
      </table>
        <a href="#/formScrum">
          <q-btn class="botonApp float-right" glossy label="Agregar" icon="person_add"  />
        </a>
    </div>
  </div>
</template>

<script>
import '../css/estilos.css'

export default {
  name: 'PageIndex'
}
</script>
