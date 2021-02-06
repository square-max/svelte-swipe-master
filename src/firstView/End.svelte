<script>


  function refresh() {
        setTimeout(function () {
            location.reload()
        }, 100);
    }

   

</script>

<div class="flex-container container">
<div>
<h1>Ingen elsker deg</h1>
<img src="./images/no-more-use.jpg" alt="ingen flere fond">
<p>Du likte desverre ingen fond, men fortvil ikke. Det finnes flere fond i havet. Sjekk dem ut her: <a href="https://www.storebrand.no/privat/fondslister"> storebrand.no </a> </p>
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