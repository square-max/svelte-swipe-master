<script>
import {Main} from "../src/index.js";
import Modal from "../src/firstView/Modal.svelte";
</script>

<div class="container">
  <div class="row">
    <div class="col">
    <img class="heart-1" src="images/Heart-pink-05.svg" alt="heart">

      <h1 class="tittel">FOND OF YOU</h1>
      <p class="top-description">Finn fondet for deg</p>
    </div>
  </div>

<Modal>
  <Main/>
</Modal>
</div>

<style>

	
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Satisfy&display=swap');

.col {
 
  background-color: #da291c;
  text-align: center;
  color: #ffffff;
  margin-bottom: 20px;

}

.tittel{ 
  margin-top: 10px;
    color: #ffffff;
    font-family: 'Ubuntu', sans-serif;
}

.heart-1 {
  position: absolute;
  overflow: hidden;
}

.heart-1 {
right: 4%;
top: 20px;
 width: 60px;
  height: auto;
 
}



.top-description {
  color: #ffffff;
    font-family: 'Satisfy', cursive;
    font-size: 15pt;
}

.container {
 max-width: 720px;
  background-color: #f5f5f5;
}


</style>