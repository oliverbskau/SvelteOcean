<script>
	import Sun from "./components/sun/Sun.svelte"
	import Water from "./components/water/Water.svelte"
	import Rick from "./pages/rick/Rick.svelte"

	function startApplication(){
		document.getElementById("startBtn").hidden = true;
		document.getElementById("content").hidden = false;
		document.getElementById("sharkGif").hidden = true;
		document.body.style.backgroundColor = "lightblue";
	}

</script>

<main>

	<div id="startBtn">
		<button on:click={startApplication}>Start App</button>
		<h3>BE AWARE OF DAY 3!</h3>
	</div>
	
	<div id="content" hidden>
		<Sun/>
		<Water/>
	</div>

	<div id="rick" hidden>
		<Rick/>
	</div>
	
	
	
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}


	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

	#startBtn{
		font-size: 100px;;
	}
</style>