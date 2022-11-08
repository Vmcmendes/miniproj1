
<template>

  <p>Vitor Mendes</p>
  <p>idade {{anos}} anos</p>
	<p>Braga Portugal</p>
	<a class="email" href="mailto:vmendes.1962@gmail.com">email</a>
		
</template>

<script>
export default {
  name: 'QuemSou',
  data() {
    return {
      anos
    }
  }
  
}
	var dataNascimento = new Date(1962,9,18);
	var hoje = new Date();
	var anos = hoje.getFullYear()-dataNascimento.getFullYear();
  if (hoje.getMonth() < dataNascimento.getMonth()) {
      anos--
}
</script>
<style>
</style>