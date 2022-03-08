<script>
	let incidents = [
  {"id": "1", 
   "date": "1646747445",
   "criticality": "HIGH",
   "state": "planned",
   "description":"Deploy new release"
  },
  {"id": "2", 
   "date": "1646747445",
   "criticality": "LOW",
   "state": "planned",
   "description":"User access investigations"
  },
  {"id": "3", 
   "date": "",
   "criticality": "MEDIUM",
   "state": "planned",
   "description":"Cleanup of files"
  },
  {"id": "4", 
   "date": "1646727445",
   "criticality": "HIGH",
   "state": "done",
   "description":"Atomic bomb dismantling"
  },
  {"id": "5", 
   "date": "1646727445",
   "criticality": "LOW",
   "state": "done",
   "description":"Some database update"
  }
];
</script>

<style>
	.HIGH {
		color: red;
	}
	.MEDIUM {
		color: orange;
	}
	.LOW {
		color: green;
	}
		.wrapper {
		border-radius: 1em;
		border-width: 1px;
		border-style: solid;
		padding:1em
	}
	
	.row {
 	 display: flex;
	}

	.column {
  	flex: 20%;
	}
	ul {
		list-style: none
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
				{new Date(incident.date)}
				</div>
			</div>
			<div class="row">
				<div class="col w-20">
					<p class="{incident.criticality}">
					{incident.criticality}
					</p> 	
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



