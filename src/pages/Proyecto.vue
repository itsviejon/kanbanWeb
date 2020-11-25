<template>
  <div class="q-pa-xl" style="margin-left:10%; margin-right:10%; ">
    <div class="q-pa-xl">
      <q-table
        hide-pagination
        :data="data"
        :columns="columns"
        title="Proyectos"
        row-key="name"
      />
       <q-btn align="between" class="btn-fixed-width q-mt-xl" color="blue-10" label="Agregar" icon="add_circle_outline" />
    </div>
  </div>
</template>

<script>
import '../css/estilos.css'

export default {
  data () {
    return {
      columns: [
        {
          name: 'name',
          required: true,
          label: '#',
          align: 'center',
          field: row => row.name,
          format: val => `${val}`,
          sortable: true
        },
        { name: 'clave', align: 'center', label: 'Clave', field: 'clave', sortable: true },
        { name: 'nombre', align: 'center', label: 'Nombre', field: 'nombre', sortable: true },
        { name: 'tableroKanban', align: 'center', label: 'Tablero Kanban', field: 'tableroKanban' },
        { name: 'actualizar', align: 'center', label: 'Actualizar', field: 'actualizar' }
      ],
      data: [
        {
          name: '1',
          clave: 'sads',
          nombre: 'SISA',
          fat: '',
          carbs: ''
        }
      ]
    }
  }
}
</script>
