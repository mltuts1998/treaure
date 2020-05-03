<template>
  <div class="home">
<a class="btn-floating aala btn-large z-depth-6 waves-effect waves-light red" id="snap"
  style="position:absolute;bottom:90px;left:10px;" 
  @click="$router.push('/games')"
><i title="About" class="material-icons"
            >format_color_text</i></a>

            <a class="btn-floating aala btn-large z-depth-6 waves-effect waves-light red" id="snap"
  style="position:absolute;bottom:90px;right:10px;" 
  @click="$router.push('/dash')"
><i title="About" class="material-icons"
            >dashboard</i></a>
		<template>
  <v-carousel cycle height="100vh" :show-arrows="false"	>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</template>



<!-- <form> -->
			<div class="fform">
			<div class="form">
			<div class="row">
    <div class="input-field col s12" style="padding-top: 10px;">
      <input value="" id="username" type="text" class="validate" v-model="username">
      <label class="active" for="username"><i class="material-icons prefix">account_circle</i></label>
    
    </div>

  </div>
			<div class="row">
    <div class="input-field col s12" style="padding-top: 10px;">
      <input value="" id="password" type="password" class="validate" v-model="password">
      <label class="active" for="password"><i class="material-icons prefix">lock_open</i></label>
    
    </div>
	
  </div>
        <button class="btn waves-effect waves-light" type="" name="action" @click="validate_data()">Login
    <i class="material-icons right">send</i>
  </button>
		</div>
		</div>
  </div>
</template>

<script>
import axios from 'axios';
 export default {
    data () {
      return {
        items: [
        {
            src: 'https://images.pexels.com/photos/459762/pexels-photo-459762.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940',
          },
          {
            src: 'https://images.pexels.com/photos/366791/pexels-photo-366791.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940',
          },
          {
            src: 'https://www.highreshdwallpapers.com/wp-content/uploads/2014/04/Game-of-Thrones-Season-1-HD-Background.jpg',
          },
          
        ],
        username:"",
        password:""
      }
    },
    methods: {
    	validate_data: function(){

      		axios.get("https://myaccount-f95bf.firebaseio.com/credentials.json/").then((req)=>{
      				let data = req.data
      				for(let key in data){
      					console.log(this.username +" "+data[key].username)
      					console.log(this.password +" "+data[key].password)
    					if(this.username == data[key].username && this.password == data[key].password){
    						localStorage.setItem("username",this.username)
                localStorage.setItem("key", key)
    						this.$router.push("/game/1")
    					}	else{
                document.querySelectorAll("input")[0].value = null; 
                document.querySelectorAll("input")[0].placeholder = "Invalid Credentials";
              }
    				}

    		})
    	}
    },
  }
</script>

<style scoped>
	.fform{
		position: absolute;
		width: 100%;
		top: 0px;
		height: 100vh;
	}
	.form{
		width:60%;
		margin: 10vh auto;
		padding: 20px;
		background: rgba(0, 0, 0, .6);
		border-radius: 10px;
		color: white;
		text-align: center;
	}
	button{
		background: rgba(0, 0, 0, 1);

	}
	

	@media screen and (max-width:1000px){
		.form{
			width: 70%;
		}
	}

	@media screen and (max-width:700px){
		.form{
			width: 90%;
		}
	}
	input{
		background: transparent;
		text-align: center;
	}

  .aala{
    animation: shake 200ms linear infinite alternate;
  }

  @keyframes shake{
    from{
      transform: translateX(-1px);
    }to{
      transform: translateX(1px);
    }
  }
</style>
