<template>  
  <div>
    <div id="slogan" class="text-center">
      <h1>Portfólio</h1>      
      <h5 class="text-secondary">Administração de Portfólio para Desenvolvedores <span class="fa fa-code"></span></h5>
    </div>
    <div id="main" class="">
      <div class="container">
        <div class="row row-main">
          <div class="col col-xs col-main">
            <h4>Habilidades</h4>
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li class="list-group-item" v-for="(habilidade,index) in habilidades" v-bind:key="index">
                    {{ habilidade }}
                  </li>                  
                </ul>
              </div>
            </div>
          </div>
          <div class="col col-xs col-main">     
            <h4>Experiências</h4> 
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li class="list-group-item" v-for="(experiencia,index) in experiencias" v-bind:key="index">
                    {{ experiencia }}
                  </li>                  
                </ul>
              </div>
            </div>      
          </div>
        </div>
        <div class="row row-main">
          <div class="col col-xs col-main">
            <h4>Link's</h4>
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li class="list-group-item" v-for="(link,index) in links" v-bind:key="index">
                    <a :href="link.url" target="blank"> {{ link.name }} </a>
                  </li>                  
                </ul>
              </div>
            </div>
          </div>
          <div class="col col-xs col-main">            
            <h4>Sobre mim</h4>
            <div class="card">
              <div class="card-body">
              </div>
            </div>
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
	name: "App",
	components: {
	},
	data: () => {
		return {
			habilidades: ["Delphi", "SQL-Server", "Oracle", "VueJS", "NodeJS", "JavaScript"],
			experiencias: ["15 anos em desenvolvimento","Orientação a Objetos","ERP-Modular","Integrações e Automações Comercias"],
			links: [{name:"Github", url:"https://github.com/"},{name:"Linkedin", url:"https://br.linkedin.com/"}]
		};
	}
};
</script>

<style>
  #slogan {
    margin-bottom: 30px;
    margin-top: 30px;
  }
  #main {
    background-color: #F17F04F8;
    padding-bottom: 30px;
    padding-top: 30px;
  }
  .row-main {
    padding-top: 20px;
    padding-bottom: 20px;
  }
  .col-main {
    color: #f1f1f1;
    min-width: 300px;
  }
  li:hover {
    font-weight: bold;
    background-color: gray;
    color: white;
  }
  a {
    text-decoration-style: none;
    text-decoration-line: none;
    color: black;    
  }

</style>
