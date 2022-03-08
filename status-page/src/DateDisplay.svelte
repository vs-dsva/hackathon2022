<svelte:options tag="date-display" />
<script>
	export let events = [];
	const months = ["Jan", "Feb", "Mar", "Apr", "Mai", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]; 

	const monthDay = (timestamp) => {
		const d = new Date(timestamp * 1000);
		return "" + d.getDay() + " " + months[d.getMonth()];
	}
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
				<div class="col col-md-3">
					<b>{monthDay(event.date)}</b>		
				</div>
				<div class="col col-md-7">
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