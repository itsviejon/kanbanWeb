<template>
  <q-page class="">
    <div class="row">
      <div class="col-md-12">
         <q-table
         :data='rows'
          title="Tablero KANBAN"
          row-key="name"
          />
      </div>
    </div>
  </q-page>
</template>

<script>
var timeElapsed = Date.now()
var today = new Date(timeElapsed)
import '../css/estilos.css'
export default {
  name: 'Index',
  data () {
    return {
      rows: [
        {
          name: 'SIAN',
          prioridad: 'Alta',
          estatus: 'Alta',
          fechaEstatus: today.toLocaleDateString(),
          development: 'Diego Calderón'
        }
      ]
    }
  }
}
</script>
