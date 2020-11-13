<template>
  <q-page class="">
    <div class="barraCabecera">
      <h4>TABLERO KANVAN</h4>
    </div>
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
    <q-circular-progress
      indeterminate
      size="45px"
      :thickness="1"
      color="black-8"
      track-color="red"
      class="q-ma-md"
    />
      </div>
    </div>
  </q-page>
</template>
<script>
var timeElapsed = Date.now()
var today = new Date(timeElapsed)
var puntoRojo = new Image()
puntoRojo.src = 'https://pbs.twimg.com/profile_images/3128936914/4c326de0f1b551ffce5c85487cf473c3.jpeg'
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
