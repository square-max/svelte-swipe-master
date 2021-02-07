<script>
	export let description = undefined;
	export let name = undefined;
</script>


<div class="white-back">
<h1>{name}</h1>
<span>
	{description}
</span>
</div>



<style>

  h1 {
		font-size: 1.5rem;
		text-align: left;
		color: #000000;
		
	}

	.white-back {
		background-color: #ffffff;
		color: #000000;	
		padding: 15px;
		border-radius: 10px;
	
	}

.white-back span{ 
	font-size: 11pt;
	line-height: 1.2;
}

</style>
