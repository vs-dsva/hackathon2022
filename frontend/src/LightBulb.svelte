<script>
	let items = ['ala', 'bala'];
	let showAlert = false;
	let onClick = function() {
		showAlert = true;
		setTimeout(function() {
			showAlert = false;
		}, 1000);
	}
</script>
<style>
	.wrapper {
		padding:1em
	}
 
</style>
<div class="panel">
	<div class="wrapper">
	<div class="row align-items-center">
		<div class="col col-md-4">
			<img class ="img-thumbnail" src="https://cdn.builder.io/api/v1/image/assets%2FTEMP%2F7e46939d4dd9451e9da4b7f153a90b05"/>
		</div>
		<div class="col">
			<ul class="list-group">
			{#each items as item}
				<li class="list-group-item">
					<div class="row">
						<div class="col-sm-8">
							{item}
						</div>
						<div class="col-sm-3">
							<div class="vismaicon vismaicon-dynamic vismaicon-add-circle" on:click="{onClick}"></div>      
						</div>
					</div>
				</li>
			{/each}
			</ul>		
		</div>
	</div>
	</div>
</div>
{#if showAlert}
<div class="alert alert-success" role="alert">
   <strong>Not implemented!</strong>It's only a day in hackathon.
</div>
{/if}
