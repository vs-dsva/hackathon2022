<script>
	export let events = [{"date":"20 May", "title":"Title1", "description":"Lorem ipsum dolor sit amet"},
							{"date": "21 May", "title":"Title2", "description":"Lorem ipsum dolor sit amet"}];
</script>
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