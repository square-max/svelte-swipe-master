<script>
	export let name = undefined;
	export let link = undefined;
	export let image = undefined;


	
</script>


<div class="pop-img">
<img alt="bilde" src={image}/>
</div>
<h1 >Det er en Match! </h1>
<p>Du og {name} liker hverandre!</p>
<a href={link} target="_blank" >Besøk meg her ;) </a>




<style>
  h1 {
		font-size: 2rem;
		text-align: center;
		font-family: 'Satisfy', cursive;
	}

@import url('https://fonts.googleapis.com/css2?family=Satisfy&display=swap');

img{
	width: 40%;
	max-width: 400px;
	margin-left:auto;
	margin-right: auto;
	margin-bottom: 20px;
	display: block;
	border-radius: 60px;
	border: 1px solid;
	border-color: #ffffff; 

}

a {
	text-align: center;
	width:50%;
		margin-left:auto;
	margin-right: auto;
	display: block;
	color: #ffffff;
	border: 1px solid;
	border-color: #ffffff;
	border-radius: 40px;
	padding: 10px 0px 10px 0px;
}

p{
	font-size: 1.3rem;
		text-align: center;
		font-family: 'Satisfy', cursive;
		text-align: center;
		margin-bottom: 20px;
}




</style>

