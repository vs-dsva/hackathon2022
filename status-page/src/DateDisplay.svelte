<svelte:options tag="date-display" />
<script>
	export let events = [];
</script>

<style>
	/* @import "https://visma-unified-design.s3.eu-north-1.amazonaws.com/latest/dist/css/vud.min.css"; */
</style>

<div class="panel">
	<ul class="list-group">
		<li class="list-group-item list-group-title">Planned events</li>
		{#each events as event}
		<li class="list-group-item">
			<div class="row">
				<div class="col w-5">
					{event.date}		
				</div>
				<div class="col w-95">
					<div class="row">
						<b>{event.title}</b>
					</div>
					<div class="row">
						{event.description}
					</div>
				</div>
			</div>
		</li>
		{/each}
	</ul>
</div>