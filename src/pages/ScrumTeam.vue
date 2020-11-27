<template>
 <div class="q-pa-xl" style="margin-left:10%; margin-right:10%; ">
    <div class="q-pa-xl">
      <q-table hide-pagination
        :data="data"
        :columns="columns"
        title="SCRUM TEAM"
        row-key="name"
      >

      <template v-slot:body="props">
        <q-tr :props="props">
          <q-td
            v-for="col in props.cols"
            :key="col.name"
            :props="props"
          >
            {{ col.value }}
          </q-td>
          <q-td auto-width>
            <q-btn align="center" class="btn-fixed-width q-mt-sm" color="blue-10"  icon-right="create" @click="medium = true"/>
          </q-td>
        </q-tr>
      </template>
      </q-table>
    </div>
    <q-dialog
      v-model="medium"
    >
    <div style="width:15%; background-color: white" >
      <q-select color="grey-3" outlined label-color="orange" v-model="model" :options="options" label="Rol">
        <template v-slot:append>
          <q-icon name="person_pin" color="orange" />
        </template>
      </q-select>
    </div>
    </q-dialog>
  </div>
</template>
<script>
import '../css/estilos.css'

export default {
  data () {
    return {
      model: null,
      medium: false,
      options: [
        'Scrum Master', 'Product Owner', 'Developer'
      ],
      columns: [
        { name: 'name', required: true, label: '#', align: 'center', field: row => row.name, format: val => `${val}`, sortable: true },
        { name: 'clave', align: 'center', label: 'CLAVE', field: 'clave', sortable: true },
        { name: 'nombre', align: 'center', label: 'NOMBRE', field: 'nombre', sortable: true },
        { name: 'rol', align: 'center', label: 'ROL', field: 'rol' },
        { label: 'OPCIONES', align: 'center' }

      ],
      data: [
        {
          name: '1',
          clave: 'Clave',
          nombre: 'Nombre',
          rol: 'rol'
        },
        {
          name: '2',
          clave: 'Clave',
          nombre: 'Nombre',
          rol: 'rol'
        },
        {
          name: '3',
          clave: 'Clave',
          nombre: 'Nombre',
          rol: 'rol'
        }
      ]
    }
  }
}
</script>
