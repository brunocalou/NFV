<template>
<div>
	<footer class="mdl-mini-footer mdl-layout--large-screen-only mdl-color--grey-900">
	  <div class="mdl-mini-footer__left-section">
	    <div class="mdl-logo">Alunos</div>
	    <ul class="mdl-mini-footer__link-list">
		  	<li v-for="name in names">
		    	{{name}}
		    </li>
	    </ul>
	  </div>
	</footer>
	<footer class="mdl-mega-footer mdl-layout--small-screen-only mdl-color--grey-900">
		<div class="mdl-mega-footer__middle-section">
		<div class="mdl-mega-footer__drop-down-section">
		  <input class="mdl-mega-footer__heading-checkbox" type="checkbox" checked>
		  <h1 class="mdl-mega-footer__heading">Alunos</h1>
		  <ul class="mdl-mega-footer__link-list">
		    <li v-for="name in names">
		    	{{name}}
		    </li>
		  </ul>
		</div>
	</footer>
</div>
</template>

<script>
export default {
	data () {
		return {
			names: ["Bruno Calou", "Heitor Guimarães", "Marcelo Maestrelli", "Rodrigo Siqueira", "Glauber Rocha", "Jhonatas Alfradique", "Caio Ramos"]
		}
	}
}
</script>