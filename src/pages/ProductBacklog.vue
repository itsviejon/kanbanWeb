<template>
  <q-page class="q-pa-md">
    <div class="q-pa-xl">
      <q-table hide-pagination
        :data="data"
        :columns="columns"
        title="Product Backlog"
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
            <q-btn align="center" class="btn-fixed-width q-mt-sm" color="red-10"  @click="medium = true"/>
          </q-td>
        </q-tr>
      </template>
      </q-table>
      <q-btn align="center" class="btn-fixed-width q-mt-sm" color="red-10" icon="add" @click="inception = true"/>
    </div>
    <q-dialog v-model="inception" full-height>
      <q-card style="width: 700px; max-width: 80vw;">
        <q-card-section>
          <div class="text-h6">Nueva Funcionalidad</div>
        </q-card-section>
        <q-card-section  >
            <q-form
                @submit="onSubmit"
                class="q-gutter-xl"
              >
              <q-input
                filled
                v-model="nombre"
                label="Funcionalidad"
                lazy-rules
              />
              <q-input
                filled
                v-model="clave"
                label="Clave del proyecto"
                lazy-rules
              />
              <q-select v-model="model" :options="options" label="Prioridad" />
              <q-input v-model="text" label="Estatus" />
              <q-select v-model="model" :options="developer" label="Desarrolladores" />
              <div>
              <q-btn flat label="Agregar" type="submit" v-model="accept"/>
              <q-btn flat label="Cerrar" v-close-popup />
              </div>
           </q-form>
         </q-card-section>
        </q-card>
      </q-dialog>
  </q-page>
</template>
<script>
import '../css/estilos.css'

export default {
  name: 'Index',
  data () {
    return {
      text: '',
      nombre: null,
      clave: null,
      date: null,
      dateend: null,
      inception: false,
      medium: false,
      model: null,
      accept: false,
      options: [
        'Alta', 'Media', 'Baja'
      ],
      columns: [
        { name: 'clave', align: 'center', label: 'CLAVE', field: 'clave', sortable: true },
        { name: 'product', align: 'center', label: 'PRODUCT BACKLOG', field: 'product' },
        { name: 'developer', label: 'DEVELOPER', align: 'center', field: 'developer' },
        { align: 'center', label: 'PRIORIDAD' }
      ],
      data: [
        {
          clave: 'Clave',
          product: 'Nombre',
          developer: 'rol'
        },
        {
          clave: 'Clave',
          product: 'Nombre',
          developer: 'rol'
        },
        {
          clave: 'Clave',
          product: 'Nombre',
          developer: 'rol'
        }
      ]
    }
  }
}
</script>
