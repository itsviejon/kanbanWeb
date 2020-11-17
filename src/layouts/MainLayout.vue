<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="barraCabecera">
      <q-toolbar>
        <q-btn
          flat
          dense
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
        <q-toolbar-title class="titulo">
          Tablero Kanban
        </q-toolbar-title>
      </q-toolbar>
      <div class="row menuText" style="padding-left:15%">
          <div class="col-md-2">
            <h5>Proyecto:</h5>
            <q-input filled  dense="dense"  label="SIAN" label-color="green"/>
          </div>
          <div class="col-md-2">
            <h5>Fecha Estatus: </h5>
            <q-input  filled  dense="dense"  label="Fecha Status" label-color="green"/>
          </div>
          <div class="col-md-2">
            <h5>Product Owner: </h5>
            <q-input filled  dense="dense"  label="Product Owner" label-color="green"/>
          </div>
          <div  class="col-md-2">
            <h5>Scrum Master: </h5>
            <q-input filled dense="dense"  label="Scrum master" label-color="green"/>
          </div>
          <div  class="col-md-3 textos" >
            <h5>Status: </h5>
            <q-input class="float-left" filled dense="dense"  label="En proceso" label-color="green"/>
          </div>
        </div>
    </q-header>
    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
    <q-scroll-area style="height: calc(100% - 150px); margin-top: 150px; border-right: 1px solid #ddd " >
      <q-list padding class="menu-list">
        <q-item clickable to="/" v-ripple>
          <q-item-section avatar>
            <q-icon name="table_view" />
          </q-item-section>
          <q-item-section>
            Tablero Kanban
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple to="/proyecto">
          <q-item-section avatar>
            <q-icon name="event_available" />
          </q-item-section>
          <q-item-section>
            Proyecto
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple to="/productBacklog">
          <q-item-section avatar>
            <q-icon name="list_alt" />
          </q-item-section>
          <q-item-section>
            Product Backlog
          </q-item-section>
        </q-item>
        <q-item clickable to="/scrumTeam" v-ripple>
          <q-item-section avatar>
            <q-icon name="people" />
          </q-item-section>
          <q-item-section >
            Scrum Team
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple to="/informes">
          <q-item-section avatar>
            <q-icon name="poll" />
          </q-item-section>
          <q-item-section>
            Informes
          </q-item-section>
        </q-item>
          </q-list>
          </q-scroll-area>
        <q-img
          class="absolute-top"
          src="https://cdn.quasar.dev/img/material.png"
          style="height: 150px"
        >
          <div class="absolute-bottom bg-transparent">
            <q-avatar size="56px" class="q-mb-sm">
              <img src="https://cdn.quasar.dev/img/boy-avatar.png" />
            </q-avatar>
            <div class="text-weight-bold">Enrique Flores</div>
          </div>
        </q-img>
    </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import '../css/estilos.css'
export default {
  name: 'MainLayout',
  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
