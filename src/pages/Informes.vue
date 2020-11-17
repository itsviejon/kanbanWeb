<template>
    <q-page>
        <div class="informeProyectos">
            <div class="titulo">
                <h4>Informes Proyectos</h4>
            </div>
            <div class="tabla">
                <table class="content-table">
                    <thead>
                    <tr>
                        <th>Proyecto</th>
                        <th>Product Backlog</th>
                        <th>Estatus</th>
                        <th>Avance (%)</th>
                        <th>Product Owner</th>
                        <th>Scrum Master</th>
                        <th>Development</th>
                    </tr>
                    </thead>
                    <tbody>
                    <tr>
                        <td>SIAN</td>
                        <td>6</td>
                        <td>1</td>
                        <td>55%</td>
                        <td>Fernando Arteaga</td>
                        <td>Saúl Landa</td>
                        <td>Diego Calderón</td>
                    </tr>
                    <tr>
                        <td>SACEC</td>
                        <td>4</td>
                        <td>2</td>
                        <td>70%</td>
                        <td>José López</td>
                        <td>Eduardo López</td>
                        <td>José Flores</td>
                    </tr>
                    <tr>
                        <td>EBIND</td>
                        <td>3</td>
                        <td>0</td>
                        <td>20%</td>
                        <td>Pedro Fuentes</td>
                        <td>Benito Martínez</td>
                        <td>Miguel Torres</td>
                    </tr>
                    </tbody>
                </table>
            </div>
        </div>
        <div class="informeKanban">
            <div class="titulo">
                <h4>Informe Tablero Kanban</h4>
            </div>
            <div class="tabla">
                <table class="content-table">
                    <thead>
                    <tr>
                        <th>Proyecto</th>
                        <th>Product Backlog</th>
                        <th colspan="3">Prioridad <br> <p> Alta Media Baja </p></th>
                        <th colspan="4">Estatus <br> <p>Pendiente Seleccionado Proceso Terminado</p></th>
                        <th>Avance (%)</th>
                    </tr>
                    </thead>
                    <tbody>
                    <tr>
                        <td>SIAN</td>
                        <td>5</td>
                        <td>1</td>
                        <td>2</td>
                        <td>2</td>
                        <td>3</td>
                        <td>2</td>
                        <td>1</td>
                        <td>1</td>
                        <td>55%</td>
                    </tr>
                    <tr>
                        <td>SACEC</td>
                        <td>5</td>
                        <td>1</td>
                        <td>2</td>
                        <td>2</td>
                        <td class="prioridad">3</td>
                        <td class="prioridad">2</td>
                        <td class="prioridad">1</td>
                        <td class="prioridad">1</td>
                        <td>70%</td>
                    </tr>
                    <tr>
                        <td>EBIND</td>
                        <td>2</td>
                        <td>1</td>
                        <td>2</td>
                        <td>2</td>
                        <td>3</td>
                        <td>2</td>
                        <td>1</td>
                        <td>1</td>
                        <td>20%</td>
                    </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </q-page>
</template>
<script>
import '../css/estilos.css'
export default {
  name: 'Informes'
}
</script>
