<template>
  <h1>Curriculum Vitae</h1>
  <div class="corpo">
	<img src="./assets/foto.jpg" alt="displayed" class="photo" />
	<h2 @click="QuemSouVisible=!QuemSouVisible">Quem sou eu?</h2>
	<QuemSou v-if="QuemSouVisible"/>
	<h2 @click="QueFacoVisible=!QueFacoVisible">O que faço</h2>
	<QueFaco v-if="QueFacoVisible"/>
	<h2 @click="MeusHobbiesVisible=!MeusHobbiesVisible">Os meus hobbis</h2>
	<MeusHobbies v-if="MeusHobbiesVisible"/>
  </div>
  <footer>
    <a href="https://www.facebook.com/vitormanuel.mendes.1/" class="fa fa-facebook"> facebook</a>
    <a href="https://twitter.com/VMendes1962" class="fa fa-twitter"> Twitter</a>
  </footer>
</template>

<script>
import MeusHobbies from "./components/MeusHobbies.vue";
import QueFaco from "./components/QueFaco.vue";
import QuemSou from "./components/QuemSou.vue";

export default {
  name: "App",
  components: {
	MeusHobbies,
    QueFaco,
    QuemSou
  },
  data() {
    return {
		count: 0,
		QuemSouVisible:false,
		QueFacoVisible:false,
		MeusHobbiesVisible:false
    }
  }
};
</script>


<style>
#app {
  font: 14px "Lucida Grande", "Trebuchet MS", Verdana, sans-serif;
  color: gray;
  margin: 0 auto;
  max-width: 300px;
  text-align: center;
  padding: 5px;
}


img    {
    border-radius: 50%;
}

h1,
h2 {
  font-family: Georgia;
  text-align: center;
}

h1 {
  border-bottom: 3px solid #aaa;
  background-color: #3b3b3b;
  color: #ddd;
  padding: 5px;
}

h2 {
  border-top: 1px solid #ccc;
  border-bottom: 1px solid #ccc;
  background-color: #ddd;
  padding: 5px;
}
p {
  line-height: 2px;
}
footer{

	height: 50px;
	bottom: 0;
	
}

.fa {
	padding: 0px;
	font-size: 20px;
	text-decoration: none;
 }
  
 
 .fa:hover {
	opacity: 0.7;
  }
  
 
  /* Facebook */
  .fa-facebook {
	background: #3B5998;
	color: white;

	
  }
  
  /* Twitter */
  .fa-twitter {
	background: #55ACEE;
	color: white;
	
  }
</style>
