<template>
  <div>
    <div id="slogan" class="text-center">
      <h1>Namecon</h1>
      <br>
      <h6 class="text-secondary">Gerador de nomes utilizando Vue.js, GraphQL e Node.js</h6>
    </div>
    <div id="main">
      <div class="container">
        <div class="row">
          <div class="col-md">
            <h5>Prefixos <span class="badge badge-info">{{ prefixes.length}}</span></h5>
            <div class="card">
              <div class="card-body">
                <ul class="list-group" v-for="prefix in prefixes" v-bind:key="prefix">
                  <li class="list-group-item"> {{ prefix }} </li>
                </ul>
                <br>
                <input type="text" class="form-control" placeholder="Digite o prefixo">
              </div>
            </div>
          </div>
          <div class="col-md">
            <h5>Sufixos <span class="badge badge-info">{{ sufixes.length }}</span></h5>
            <div class="card">
              <div class="card-body">
                <ul class="list-group" v-for="sufix in sufixes" v-bind:key="sufix">
                  <li class="list-group-item"> {{sufix}} </li>
                </ul>
                <br>
                <input type="text" class="form-control" placeholder="Digite o sufixo">
              </div>
            </div>
          </div>
        </div>
        <br>
        <h5>Domínios <span class="badge badge-info">{{ domains.length}}</span></h5>
        <div class="card">
          <div class="card-body">
              <ul class="list-group" v-for="domain in domains" v-bind:key="domain.name">
                <li class="list-group-item">{{domain}}</li>
              </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import "font-awesome/css/font-awesome.css";

export default {
  name: 'App',
  data() {
    return {
      prefixes: ['Air', 'Jet', 'Flight'],
      sufixes: ['Hub', 'Station', 'Fly'],
      domains: ['AirStation', 'JetFly', 'FlightHub']
    }
  }
}
</script>

<style>
#slogan {
  margin-top: 30px;
  margin-bottom: 30px;
};

#main {
  background-color: #f1f1f1;
  padding-top: 30px;
  padding-bottom: 30px;
}
</style>
