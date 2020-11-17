<template>
  <div class="q-pa-md" style="margin-left:30%; margin-right:30%; ">
    <div class="titulo">
      <h4>Agregar Integrante</h4>
    </div>
    <div class="q-pa-md">
      <q-form
      @submit="onSubmit"
      class="q-gutter-md"
    >
      <q-input
        autocomplete="off"
        v-model="nombre"
        label="Nombre"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Campo obligatorio']"
      />
      <q-input
        autocomplete="off"
        v-model="apellidoM"
        label="Apellido Materno"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Campo obligatorio']"
        />
      <q-select v-model="rol" :options="options" label="Rol" />
      <div>
        <q-btn label="Agregar" type="submit" color="primary" icon="person_add" class="float-right"/>
      </div>
    </q-form>
    </div>
  </div>
</template>

<script>
import '../css/estilos.css'

export default {
  data () {
    return {
      name: 'PageIndex',
      nombre: null,
      apellidoM: null,
      rol: null,
      accept: false,
      options: [
        'Scrum Master', 'Product Owner', 'Development'
      ]
    }
  },
  methods: {
    onSubmit () {
      if (this.accept !== true) {
        this.$q.notify({
          color: 'green-4',
          textColor: 'white',
          icon: 'check_circle_outline',
          message: 'Integrante agregado'
        })
      }
      this.nombre = null
      this.apellidoM = null
    }
  }
}
</script>
