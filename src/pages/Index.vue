<template>
  <q-page class="">
    <div class="qa-pa-md tabla">
      <div class="row">
      <div class="col-md-8 offset-md-3">
         <q-table
         card-class="bg-cyan-1 text-black"
         color="primary"
         :data='rows'
          title="Tablero KANBAN"
          row-key="name"
          class="table"
          hide-bottom
          />
      </div>
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
          prioridad: '',
          estatus: '',
          fechaEstatus: today.toLocaleDateString(),
          development: 'Diego Calderón'
        }
      ]
    }
  }
}
</script>
