<template>
    <q-page>
        <div class="q-pa-xl">
            <q-table
                hide-pagination
                :data="data"
                :columns="columns"
                title="Proyectos"
                row-key="name"
            />
        </div>
    </q-page>
</template>
<script>
import '../css/estilos.css'
export default {
  name: 'Informes',
  data () {
    return {
      columns: [
        {
          name: 'number',
          required: true,
          label: '#',
          align: 'center',
          field: row => row.name,
          format: val => `${val}`,
          sortable: true
        },
        { name: 'clave', align: 'center', label: 'Clave', field: 'clave' },
        { name: 'nombre', align: 'center', label: 'Nombre', field: 'nombre' },
        { name: 'productBacklog', align: 'center', label: 'Product Backlog', field: 'productBacklog' },
        { name: 'avance', align: 'center', label: 'Avance', field: 'avance' },
        { name: 'productOwner', align: 'center', label: 'Product Owner', field: 'productOwner' },
        { name: 'scrumMaster', align: 'center', label: 'Scrum Master', field: 'scrumMaster' },
        { name: 'development', align: 'center', label: 'Desarrolladores', field: 'development' }
      ],
      data: [
        {
          number: '1',
          clave: 'sads',
          nombre: 'SISA',
          productBacklog: '5',
          avance: '55%',
          productOwner: 'José Osorio',
          scrumMaster: 'Miguel González',
          development: '8'
        }
      ]
    }
  }
}
</script>
