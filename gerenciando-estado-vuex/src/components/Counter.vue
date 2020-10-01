<template>
<div class="card text-center">
  <div class="card-header">
      <h1>Contador: {{counter}}</h1>
  </div>
  <div class="card-body">
    <h5 class="card-title">Funcional</h5>
    <button class="btn btn-danger" @click="decrement">Decrementar</button>
    &nbsp;
    <button class="btn btn-primary" @click="increment">Incrementar</button>
  </div>
  <div class="card-footer text-muted">
    Jocimar Galante
  </div>
</div>

</template>

<script>
import {mapGetters, mapActions} from 'vuex'
export default {
    name: 'Counter',
    computed: {
        ...mapGetters([
            'counter'
        ])
    },
    methods: {
        ...mapActions([
            'decrement',
            'increment'
        ])
    },

}
</script>
<style>
    .card{
        background: #FFFFFF;
        box-shadow: 4px 4px 33px rgba(0, 0, 0, 0.25);
        border-radius: 5px;
        width: 500px;
        margin: 0 auto; /* Added */
        float: none; /* Added */
        margin-bottom: 10px; /* Added */
    }
</style>