<template>
    <q-page>
        <div class="row q-gutter-sm" style="padding-left:15%">
          <div class="col-md-3">
            <h5>Proyecto:</h5>
            <q-input filled  dense="dense"  label="SIAN" label-color="green"/>
          </div>
          <div class="col-md-3">
            <h5>Fecha Estatus: </h5>
            <q-input  filled  dense="dense"  label="Fecha Status" label-color="green"/>
          </div>
          <div class="col-md-3">
            <h5>Product Owner: </h5>
            <q-input filled  dense="dense"  label="Product Owner" label-color="green"/>
          </div>
          <div  class="col-md-4 ">
            <h5>Scrum Master: </h5>
            <q-input filled dense="dense"  label="Scrum master" label-color="green"/>
          </div>
          <div  class="col-md-4" >
            <h5>Status: </h5>
            <q-input  filled dense="dense"  label="En proceso" label-color="green"/>
          </div>
        </div>
        <div class="q-pa-xl">
            <q-table
                hide-pagination
                :data="data"
                :columns="columns"
                title="Tablero Kanban"
                row-key="name"
            />
        </div>
    </q-page>
</template>

<script>
import '../css/estilos.css'
export default {
  name: 'Kanban',
  data () {
    return {
      columns: [
        { name: 'clave', align: 'center', label: 'Clave', field: 'clave' },
        { name: 'productBacklog', align: 'center', label: 'Product Backlog', field: 'productBacklog' },
        { name: 'prioridad', align: 'center', label: 'Prioridad', field: 'avance' },
        { name: 'status', align: 'center', label: 'Estatus', field: 'productOwner' },
        { name: 'fechaStatus', align: 'center', label: 'Fecha Estatus', field: 'scrumMaster' },
        { name: 'development', align: 'center', label: 'Desarrolladores', field: 'development' }
      ],
      data: [
        {
          clave: 'sads',
          productBacklog: '5',
          prioridad: '55%',
          status: '',
          fechaStatus: '',
          development: '8'
        }
      ]
    }
  }
}
</script>
