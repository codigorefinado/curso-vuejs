<template>
  <div id="app">
    <md-card>
      <md-card-header>
        <div class="md-title">Material Design Com Vue.js 2</div>
        <div class="md-suhead">Com Clayton do http://medium.com/codigorefinado e também no Youtube :D</div>
      </md-card-header>

      <md-card-content>
        <md-button class="md-raised md-primary" @click="table()">Tabela</md-button>
        <md-button class="md-raised md-primary" v-on:click="limpar()">Limpar</md-button>

        <button @click="table()">Table</button>
        <button @click="limpar()">Limpar</button>
      </md-card-content>

      <md-table>

        <md-table-header>
          <md-table-row>

            <md-table-head>Primeiro nome</md-table-head>
            <md-table-head>Sobre nome </md-table-head>
            <md-table-head>E-mail</md-table-head>

          </md-table-row>
        </md-table-header>

        <md-table-body>
          <md-table-row v-for="contato in contatos">
            <md-table-cell>{{ contato.nome }}</md-table-cell>
            <md-table-cell>{{ contato.sobrenome}}</md-table-cell>
            <md-table-cell>{{ contato.email}}</md-table-cell>
          </md-table-row>
        </md-table-body>

      </md-table>

    </md-card>

  </div>
</template>

<script>
  export default {
    name: 'app',
    data: function () {
      return {
        contatos: [
          {nome: 'Clayton', sobrenome: 'Passos', email: 'clayton.passos@gmail.com'},
          {nome: 'Daniela', sobrenome: 'Passos', email: 'daniela.passos@gmail.com'}
        ]
      }
    },
    methods: {
      table: function () {
        this.contatos.push({nome: 'Sebastian', sobrenome: 'Eschweiler', email: 's.eschweiler@mail.com'})
        this.contatos.push({nome: 'Bill', sobrenome: 'Smith', email: 'b.smith@mail.com'})
        this.contatos.push({nome: 'Ann', sobrenome: 'Parker', email: 'a.parker@mail.com'})
      },
      limpar: function () {
        this.contatos.splice(0, this.contatos.length)
      }
    }

  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
