<svelte:head>
<script type="module" src="https://md-block.verou.me/md-block.js">
</script>
	<link rel="stylesheet" href="https://nc4-visma.s3.eu-north-1.amazonaws.com/latest/dist/css/nc.min.css" type="text/css"/>
</svelte:head>
<script>
	import { onMount } from 'svelte';
	
	import Title from "./Title.svelte";
	import LightBulb from "./LightBulb.svelte";
	import PlannedMaintennance from "./PlannedMaintenance.svelte";
	import DateDisplay from "./DateDisplay.svelte"; 
	let kommune = "Not Set";
	
	export let href="/controller";
	let data = {};
	
	onMount(async () => {
		const res = await fetch(href);
		data = await res.json();
	});
</script>

<div class="container">
  <div class="row">
			<div class="col">
				<Title kommune="{kommune}"></Title>
			</div>
  </div>

  <div class="row">
    <div class="col">
			<LightBulb></LightBulb>
		</div>
    <div class="col">
			<PlannedMaintennance></PlannedMaintennance>
		</div>
    <div class="col">
			<DateDisplay ></DateDisplay>
		</div>
  </div>
</div>




