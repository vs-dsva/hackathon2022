<svelte:options tag="planned-maintenance" />
<script>
	export let incidents = [];
	let colors = {"high":"red", "medium":"orange", "low":"green`"}
</script>

<style>
	@import "https://visma-unified-design.s3.eu-north-1.amazonaws.com/latest/dist/css/vud.min.css";

	.cr-high {
		background-color: red;
	}
	.cr-medium {
		background-color: orange;
	}
	.cd-low {
		background-color: green;
	}	
</style>
<div class="panel">
	<ul class="list-group">
		<li class="list-group-item list-group-title">Log/Incidents</li>
		{#each incidents as incident}
		<li class="list-group-item">
			<div class="row">
				<div class="col w-10">
					{incident.id}		
				</div>
				<div class="col w-90">
				{new Date(incident.date * 1000)}
				</div>
			</div>
			<div class="row">
				<div class="col w-20">
					<span class="cr-{incident.level}">
					<b>{incident.level.toUpperCase()}</b>
					</span> 	
				</div>
				<div class="col w-80">
					{incident.state}						
				</div>
			</div>
			<div class="row">
					{incident.description}
			</div>
			
		</li>
		{/each}
	</ul>
</div>



