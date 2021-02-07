<script>


  function refresh() {
        setTimeout(function () {
            location.reload()
        }, 100);
    }

   

</script>

<div class="flex-container container">
<div>
<img src="./images/no-more-use.jpg" alt="ingen flere fond">
<h1>Ingen flere fond i nærheten</h1>
<p>Fortsatt ikke funnet det rette fondet for deg? Fortvil ikke, det finnes flere fond i havet. Sjekk dem ut her! <a href="https://www.storebrand.no/privat/fondslister"> storebrand.no</a> eller start på nytt.<p>
   <p> Dette er ikke et personlig investeringsråd. Storebrand anbefaler at du leser produktets prospekt og nøkkelinformasjon før du eventuelt tar en beslutning om å investere i fond.</p>

</div>


    <div class="row">
        <div class="yes-no-buttons">
        <div class="reset-but">
            <button on:click={refresh} onclick="this.blur();" class="reset">
                <strong>Start på nytt</strong>
            </button>
        </div>
        </div>
    </div>

</div>

<style>

	.yes-no-buttons {
        width: 100%;
		position: relative;
		margin-top: 20px;
        margin-bottom: 60px;
    }

    .reset-but {
		width: 100%;
        text-align: center;

    }
    .reset {
		padding: 5px 20px 5px 20px;
        margin-top: 15px;
        margin-bottom: 20px;
		border-radius: 30px;
		box-shadow: 0px 0px 4px #da291c;
        min-width: 300px;
        font-size: 10pt;

	}

    h1{
        text-align: center;
    }

    	img {
    width: 100%;
	height: auto;
    margin-bottom: 10px;
  }

	
</style>