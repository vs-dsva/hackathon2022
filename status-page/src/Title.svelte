<svelte:options tag="statuspage-title" />
<script>
	export let kommune = 'world';
</script>

<style>
	.very_big {
		font-size: 48px;
	}

	.wrapper {
		padding:1em;
	}

</style>
<div class="panel">	
	<div class="wrapper">
	<div class="row align-items-center">
		<div class="col col-md-2">
			<img  src="https://cdn.builder.io/api/v1/image/assets%2FTEMP%2F55565bdbdd8744c78d6003df1cf2d4ec" class="image"/>			
		</div>
		<div class="col col-md-6">
			<h1 class="very_big">Status for {kommune}</h1>		
		</div>
		<div class="col col-md-3">
			<div class="dropup" style="float:right">
				<button type="button" id="dropdownMenuButton1" class="btn btn-primary btn-lg btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false"> Select... </button>
				<ul class="dropdown-menu" role="menu" aria-expanded="false" aria-hidden="true" aria-labelledby="dropdownMenuButton1">
					<li><a href="#">Alta</a></li>
					<li><a href="#">Customer1</a></li>
					<li><a href="#">Atlantis</a></li>
				</ul>
				</div>
			</div>
		</div>		
	</div>
</div>
