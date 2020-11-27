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
                class="col-4"
                filled
                v-model="nombre"
                label="Nombre del proyecto"
                lazy-rules
              />
              <q-input
                class="col-4"
                filled
                v-model="clave"
                label="Clave del proyecto"
                lazy-rules
              />

              <q-input class="col-4" filled v-model="date" mask="date" :rules="['date']" label="Fecha Inicio">
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
              <q-input class="col-4" filled v-model="dateend" mask="date" :rules="['date']" label="Fecha Fin">
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
          </q-form>
        </q-card-section>

        <q-card-actions align="left" class="text-primary">
          <q-btn flat label="Agregar" type="submit" @click="accept = true"/>
          <q-btn flat label="Cerrar" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>

  </div>
  </div>
</template>

<script>
import '../css/estilos.css'
export default {
  data () {
    return {
      framework: {
        plugins: [
          'Notify'
        ],
        config: {
          notify: { /* look at QUASARCONFOPTIONS from the API card (bottom of page) */ }
        }
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
  },
  methods: {
    onSubmit () {
      if (this.accept !== true) {
        this.$q.notify({
          color: 'red-5',
          textColor: 'white',
          icon: 'warning',
          message: 'Completa los campos'
        })
      } else {
        this.$q.notify({
          color: 'green-4',
          textColor: 'white',
          icon: 'cloud_done',
          message: 'Proyecto agregado'
        })
      }
      this.nombre = null
      this.clave = null
      this.date = null
      this.dateend = null
    }
  }
}
</script>
