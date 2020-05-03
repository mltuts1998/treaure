<template>
	<div class="game" :style="[{'background': black}, {'color': white}]">
	
  <div class="row">
    <div class="col">
      <div class="card" :style="{'background': lblack}">
        <div class="card-image">
          <div class="camera" ref="camera">
          		<video id="video" autoplay></video>
				<canvas id="canvas"></canvas>
          </div>
        </div>
        <div class="card-content">
        	<h5 style="font-weight:bolder;">HINT: </h5>
          <p>{{ value }}</p>
        </div>
        <div class="card-action">
          <h6>SCAN IMAGE</h6>
          <a class="btn-floating btn-large waves-effect waves-light red alas" id="snap"><i title="scan" class="material-icons" @click="aam()"
          	>camera</i></a>
          	  <img src="https://miro.medium.com/max/1424/1*sHmqYIYMV_C3TUhucHrT4w.png" 
          	  @click="alla()" >	

        </div>
      </div>
    </div>
  </div>

  <div>
  	<a class="btn-floating btn-large waves-effect waves-light red alas" id="snap" 
  		style="position:fixed;top: 10px;right:10px;z-index:15;"><i title="Night Mode" class="z-depth-6 material-icons"
  		@click="modes()"
          	>{{ modawa }}</i></a>

    <a class="btn-floating btn-large aba waves-effect waves-light red alas" id="snap" 
  		style="position:fixed;top: 10px;right:10px;z-index:15;"><i title="Night Mode" class="z-depth-6 material-icons"
  		@click="logout()"
          	>lock</i></a>
  </div>

	</div>
</template>
<script type="text/javascript">
import axios from 'axios';
import Tesseract from 'tesseract.js';
 
 		export default{
 			data(){
 				return{
 					texts:"",
 					mode:"day",
 					black: "white",
 					lblack: "white",
 					white: "black",
 					modawa: "airline_seat_individual_suite",
 					hints:[
 					],
 					solution:[
 					],
 				}
 			}
			,
			computed:{
				value: function(){
					let a = localStorage.getItem("id")
					return this.solution[a]
				}
			},
			methods: {
				alla(){
						let text = prompt("Type The Hint If You Find A problem");
						if(localStorage.getItem("id") == 5){
								this.$router.push("/dash");
						}
						console.log(this.hints)
						if(text.toLowerCase() == this.hints[localStorage.getItem("id")].toLowerCase()){
							localStorage.setItem("id", (Number(localStorage.getItem("id"))+1))
							let ap = new Date();
							axios.patch("https://myaccount-f95bf.firebaseio.com/credentials/"+localStorage.getItem("key")+".json", {
								"key": localStorage.getItem("id"),
								"time": ap
							}).then((req)=>{
		      						console.log(req)
		      					})

							this.$router.push("/game/"+localStorage.getItem("id"))
							location.reload();		
						}
				},
				logout: function(){
					var a = confirm("are you sure you want to logout")
					var b = confirm("do you your score to be visible in dashboard")
							axios.patch("https://myaccount-f95bf.firebaseio.com/credentials/"+localStorage.getItem("key")+".json", {
								"seen": b
							}).then((req)=>{
		      						console.log(req)
		      					})
					if(a){
						localStorage.clear()
						this.$router.push("/")
					}
				},
				aam: function(){
					// Elements for taking the snapshot
var canvas = document.getElementById('canvas');
var context = canvas.getContext('2d');
var video = document.getElementById('video');
console.log(this.$refs.camera.style)
// Trigger photo take
document.getElementById("snap").addEventListener("click", function() {
	context.drawImage(video, 0, 0, 150, 100);
			Tesseract.recognize(
				canvas.toDataURL("image/jpeg",1.0),
		  'eng',
		  // { logger: m => console.log() }
		).then(({ data: { text } }) => {
		  			if(localStorage.getItem("id") == 5){
							this.$router.push("/dash");
						}
						if(text.toLowerCase() == this.hints[localStorage.getItem("id")].toLowerCase()){
							localStorage.setItem("id", (Number(localStorage.getItem("id"))+1))
							this.$router.push("/game/"+localStorage.getItem("id"))
							 location.reload();
						}

		}).catch(err=>console.log(err))

		});
				},
				modes: function(){
						if(this.mode == "day"){
							this.mode="dark",
		 					this.black= "#100E17",
		 					this.lblack= "#17141D",
		 					this.white= "white",
		 					this.modawa = "wb_sunny"
						}else{
							this.mode="day",
		 					this.black= "white",
		 					this.lblack= "white",
		 					this.white= "black",
		 					this.modawa= "airline_seat_individual_suite"
						}
				}
			},
			created(){
				axios.get("https://myaccount-f95bf.firebaseio.com/hints.json/").then((req)=>{
    				let data = req.data
    				for(let key in data){
    					this.solution.push(data[key].hints)  					
    				   	this.hints.push(data[key].solution)
    				}
    			})
			},
			mounted(){
				var video = document.getElementById('video');

// Get access to the camera!
if(navigator.mediaDevices && navigator.mediaDevices.getUserMedia) {
    // Not adding `{ audio: true }` since we only want video now
    let constraints = { video: true , facingMode:"environment"};
    navigator.mediaDevices.getUserMedia(constraints).then(function(stream) {
        //video.src = window.URL.createObjectURL(stream);
        video.srcObject = stream;
        video.play();
    });
}
			}
		}
	
</script>

<style scoped>

	.game{
		height: 100vh;
	}


	.aba{
		position: absolute;
		top: 10px;
		left: 10px;
	}
	.row > *{
		width: 100%;
		height: 100vh;
		text-transform: capitalize;
		font-family: ubuntu;
	}
	.card{
		width: 40%;
		text-align: center;
		margin: 15px auto;
	}

	.card-image{
		margin: auto;
		width: 100%!important;
		text-align: center;
		position: relative;
		top: 10px;
	}
	p{
		text-align: justify;
		font-weight: bold;
	}

	.card-action > img{
		position:absolute;
		width:10%;
		left: 5px;
		margin:auto;
		bottom: 5px;
	}
	
	.card-image{
		height: 300px;
	}
	.camera{
		position: absolute;
		top: 0;
		left: 0;
		bottom: 0;
		right: 0;
		background: white;
	}

	video, canvas{
		position: absolute;
		top:0;
		left:0;
		width: 100%!important;
		height: 100%!important;
		    object-fit: cover;
	}

	canvas{
		width: 50%!important;
		height: 50%!important;	
	}

	video{
		z-index:12;
	}
	canvas{
		z-index: 13;
	}
	.alas{
		position: absolute;
		right: 5px;
		bottom:5px;
	}

	@media (max-width:1200px){
		.card{
			width: 60%;
		}
	}
	@media (max-width:700px){
		.card{
			width: 80%;
		}
	}

	@media (max-width:400px){
		.card{
			width: 90%;
		}
	}
</style>