<template>
	<div>
		<h3 style="text-align:center;text-transform: uppercase">Score Board</h3>
	<ul class="collection">
    <li class="collection-item avatar" v-for="(a,i) in list" :key="i" v-show="a.seen">
      <img :src="`https://robohash.org/{i}.png`" alt="" class="circle">
      <span class="title" style="text-transform: uppercase">{{a.username}}</span>
      <p>Points: {{a.key}}<br>
      </p>
       <p> <b>completed tasks at</b> {{a.time}}</p>
    </li>
</ul>

<a class="btn-floating aala btn-large z-depth-6 waves-effect waves-light red" id="snap"
  style="position:absolute;top:10px;right:10px;" 
  @click="$router.push('/')"
><i title="Play" class="large material-icons"
            >home</i></a>
	</div>
</template>


<script type="text/javascript">
	import axios from "axios"
	export default{
		data(){
		return{
		list:[
		]
		}}
		,created(){
			axios.get("https://myaccount-f95bf.firebaseio.com/credentials.json/").then((req)=>{
      				let data = req.data
      				for(let key in data){
      					this.list.push(data[key])
      					console.log(this.list)
    				}
    			})
		}
	}
</script>