<template>
  <div class="q-pa-xl" style="margin-left:10%; margin-right:10%; ">
    <div class="q-pa-xl">
      <q-table
        hide-pagination
        :data="data"
        :columns="columns"
        title="Proyectos"
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
            <a href="/">
            <q-btn align="center" class="btn-fixed-width q-mt-sm" color="blue-10"  icon-right="date_range" @click="medium = true"/>
            </a>
          </q-td>
          <q-td auto-width>
            <q-btn align="center" class="btn-fixed-width q-mt-sm" color="blue-10"  icon-right="update" @click="medium = true"/>
          </q-td>
        </q-tr>
      </template>
      </q-table>
       <q-btn align="between" class="btn-fixed-width q-mt-xl" color="blue-10" label="Agregar" icon="add_circle_outline" @click="inception = true"/>
    </div>
    <div >
    <q-dialog v-model="inception" full-height>
      <q-card style="width: 700px; max-width: 80vw;">
        <q-card-section>
          <div class="text-h6">Nuevo Proyecto</div>
        </q-card-section>
        <q-card-section  >
            <q-form
                @submit="onSubmit"
                class="q-gutter-xl"
              >
              <q-input
                filled
                v-model="nombre"
                label="Nombre del proyecto"
                lazy-rules
              />
              <q-input
                filled
                v-model="clave"
                label="Clave del proyecto"
                lazy-rules
              />
              <q-input  filled v-model="date" mask="date" :rules="['date']" label="Fecha Inicio">
                <template v-slot:append>
                  <q-icon name="event" class="cursor-pointer">
                    <q-popup-proxy ref="qDateProxy" transition-show="scale" transition-hide="scale">
                      <q-date v-model="date">
                        <div class="row items-center justify-end">
                          <q-btn v-close-popup label="Close" color="primary" flat />
                        </div>
                      </q-date>
                    </q-popup-proxy>
                  </q-icon>
                </template>
              </q-input>
              <q-input filled v-model="dateend" mask="date" :rules="['date']" label="Fecha Fin">
                <template v-slot:append>
                  <q-icon name="event" class="cursor-pointer">
                    <q-popup-proxy ref="qDateProxy" transition-show="scale" transition-hide="scale">
                      <q-date v-model="dateend">
                        <div class="row items-center justify-end">
                          <q-btn v-close-popup label="Close" color="primary" flat />
                        </div>
                      </q-date>
                    </q-popup-proxy>
                  </q-icon>
                </template>
              </q-input>
              <div>
              <q-btn flat label="Agregar" type="submit" v-model="accept"/>
              <q-btn flat label="Cerrar" v-close-popup />
              </div>
           </q-form>
         </q-card-section>
        </q-card>
      </q-dialog>
    </div>
  </div>
</template>

<script>
import '../css/estilos.css'
import Notify from 'quasar'
import Vue from 'vue'
Vue.use(Notify)
export default {
  data () {
    return {
      framework: {
        plugins: [
          'Notify'
        ]
      },
      nombre: null,
      clave: null,
      date: null,
      dateend: null,
      inception: false,
      accept: false,
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
        { label: 'Tablero kanban', align: 'center' },
        { label: 'Actualizar', align: 'center' }

      ],
      data: [
        {
          name: '1',
          clave: 'sads',
          nombre: 'SISA'
        }
      ]
    }
  },
  methods: {
    onSubmit () {
      this.$q.notify({
        color: 'green-4',
        textColor: 'white',
        icon: 'cloud_done',
        message: 'Proyecto agregado'
      })
      this.nombre = null
      this.clave = null
      this.date = null
      this.dateend = null
    }
  }
}
</script>
