<script>
	import About from "./Components/About.svelte";
	import Text from "./Components/Text.svelte";
	import Person from "./Components/Person.svelte";
	import Skills from "./Components/Skills.svelte";
	import Input from "./Components/Input.svelte";
	import Photos from "./Components/Photos.svelte";
	import BottonCount from "./Components/ButtonCount.svelte";
  import ButtonCount from "./Components/ButtonCount.svelte";
	export let name;
	export let lastName;
	export let svelteLogo = "https://arepa.s3.amazonaws.com/svelte-logo.png";
	
	const data ={
		name:"David",
		lastName:"Dzul",
		age:39
	}
</script>

<style>
	:global(body){
		background-color:#f2eee2;
		color:#0084f6;
	}

	:global(:root){
		--theme-color:purple;
	}

	:global(body.dark-mode){
		background-color:#1d3040;
		color:#bfc2c7;
		
	}

	:global(body.dark-mode p span){
		background-color:#1d3040;
		color:yellow;
		
	}

	

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	main img {
		width:30%;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<h1>Hello {name} {lastName}!</h1>
	<About/>
	<Text anotherText="Hola!"/>
	<Text/>
	<Person {...data}/>
	<Skills/>
	<Input/>
	<ButtonCount/>
	<Photos/>
	<img src={svelteLogo} alt="Logo">
	
</main>