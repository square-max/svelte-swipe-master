<script>
  export let name = undefined;
	export let description = undefined;
	export let image = undefined;
	export let usp = [];
	export let descriptionCallback = undefined;
</script>
<div class="flex-container container">
	
	<div class="row p-2">
				<img src={image} alt="bilde" />
				<div class="col-md-12">
			<h3 class="name-tittel">{name}</h3>
			<div>
			</div>
		</div>
	</div>
	
	<div class="row">
		<div class="col-md-12">
			<div style="display:inline;" class="mt-3">
			{#each usp as u}
				<div style="display:inline;" class="usper"><i class="text-black">{u}</i></div>
			{/each}
			</div>
		</div>
	</div>
		
  <hr/>

	<div style="cursor:pointer;" on:click={descriptionCallback}>
		<p> {description.substring(0,280)}...</p>
		<p class="lesmer">Trykk for å lese mer</p>
	</div>

	<hr>

</div>

<style>
	img {
    width: 100%;
	height: auto;
    margin-bottom: 10px;
  }

  .name-tittel {

  padding-left: 10px;

  }

.usper {
	background-color: #ffadbc;
	margin: 0px 5px 0px 5px;
	padding: 5px 15px 5px 15px;
	border-radius: 50px;
	font-size: 12px;
}

.mt-3{
   
    margin-left: 10px;
}

.col-md-12 {
	padding-left:10px;
}

.lesmer {
	font-weight: 500;
	text-decoration: underline;
}


@media only screen and (max-width: 600px) {
 	img {
    width: 100%;
	height: auto;
	max-height: 190px;
    margin-bottom: 10px;
  }

}

</style>