<template>
	<div class="games" style="">
		<img src="../assets/01.jpg" style="position:absolute;z-index:-1;object-fit:cover;top:10px;left:0;width:100%; height:100%">
			<div class="bgded overlay" >
  <div id="pageintro" class="hoc clear" style="height: background:transparent;100vh; overflow:hiddden;"> 
    <!-- ################################################################################################ -->
    <div class="flexslider basicslider">
      <ul class="slides">
        <li>
          <article>
            <h3 class="heading">RIT Treasure Hunt</h3>
            <p>Organize Treasure Hunts Online</p>
          </article>
        </li>
      </ul>
    </div>
    <!-- ################################################################################################ -->
  </div>
</div>
<!-- ################################################################################################ -->
<div class="wrapper aaa row3" style="height:70vh;">
  <main class="hoc container clear"> 
    <!-- main body -->
    <!-- ################################################################################################ -->
    <div class="one_half first">
      <h3 class="heading font-x2">About This WebApp</h3>
      <p>This webapp has been created to help in organize Treasure Hunts in better ways by providing an online platform.</p>
      <p style="font-weight:bolder;text-decoration:underline;">Features:</p>
      <ul>
        <li>Can organize Treasure Hunts in an effective way</li>
        <li>Load next hint only on successful submission of previous hint answers</li>
        <li>Maintains time-stamp for each submission. Hence organizers can declare winners without ambiguity</li>
        <li>Easy user-interface for creators and players</li>
 <li style="font-style:italic;"><p style="text-transform:uppercase;font-size:15px;display:inline;font-weight:bolder;">optical character recognition</p> is also used</li>
        <li style="font-weight:bolder;font-style:italic;">Night mode is also available</li>
        <li style="font-weight:bolder;font-style:italic;">It's a Progressive Web App</li>
      </ul>
    </div>
    <figure class="one_half">
      <img src="../assets/about.jpg" style="min-width:100%; ">
    </figure>
    <!-- ################################################################################################ -->
    <!-- / main body -->
    <div class="clear"></div>
  </main>
</div>
<!-- ################################################################################################ -->
<!-- ################################################################################################ -->
<!-- ################################################################################################ -->
<div class="wrapper bbb bgded overlay" style="background-image:url(../assets/01.jpg); height: 30vh;">
  <article class="hoc container center" style="margin:auto;tex-align:center;"> 
    <!-- ################################################################################################ -->
    <h5 class="heading font-x3" style="padding-bottom:20px;">Ready, Set, Go</h5>
    <div class="aaaaa">
    	<a class=" a btn-floating aala btn-large z-depth-6 waves-effect waves-light red" id="snap"
  style="position:fixed;top:20px;right:20px;" 
  @click="$router.push('/')"
><i title="Play" class="large material-icons"
            >home</i></a>
    </div>

    <!-- ################################################################################################ -->
  </article>
</div>
	</div>
</template>


<script>
	export default{

	}
</script>

<style scoped>

html{
	background: #1D1D1D;
}
	.one_half > img{
		width: 50%;
	}
	.aaa{
		position: absolute;
		width: 100%;
		top: 100vh;
		height: 100vh;
	}
	main{
		height: 100vh;
		display: flex;
		margin-top: 100px;
	}
	.one_half.first{
		width: 55%;
	}

	.one_half:nth-child(2){
		width: 40%;
	}


		.a1{
			position: absolute;
			left: 50px;
			color: black;
			text-transform:uppercase;
			font-family: ubuntu;
			font-weight: bolder;
		}

	a.a {
		   animation: shake 200ms linear infinite alternate;
  }

  @keyframes shake{
    from{
      transform: translateX(-1px);
    }to{
      transform: translateX(1px);
    }
  }


@media (max-width:900px){
.one_half.first{
		width: 100%;
	}

	.one_half:nth-child(2){
		width: 40%;
	}
}


@media (max-width:800px){

main{
	display: block;
}
	.one_half:nth-child(2){
	display: none;
	}
}
.aaaa{
	margin:auto;
}

@charset "utf-8";
.row0, .row0 a{}
.row1{border-bottom:1px solid;}
.row2, .row2 a{}
.row3, .row3 a{}
.row4, .row4 a{}
.row5{border-top:1px solid;}


#pageintro{padding:250px 0;}

#pageintro li article{display:block; max-width:75%; margin:0 auto; text-align:center;}
#pageintro li article *{margin:0;}
#pageintro li p:first-of-type{margin-bottom:10px; font-style:italic;}
#pageintro li .heading{margin-bottom:30px; font-size:3rem; word-wrap:break-word;}
#pageintro li p:nth-of-type(2){line-height:1.5rem;}
#pageintro li footer{margin-top:40px;}


#topbar{padding:15px 0; font-size:.8rem; text-transform:uppercase;}

#topbar *{margin:0;}
#topbar ul li{display:inline-block; margin-right:10px; padding-right:15px; border-right:1px solid;}
#topbar ul li:last-child{margin-right:0; padding-right:0; border-right:none;}
#topbar i{margin:0 5px 0 0; line-height:normal;}

#header{}

#header #logo{margin:30px 0 0 0;}
#header #logo h1{margin:0; padding:0; font-size:22px; text-transform:uppercase;}


.container{padding:80px 0;}
.container .content{}

.sectiontitle{display:block; max-width:65%; margin:0 auto 60px; text-align:center;}
.sectiontitle *{margin:0;}

.services{}
.services > li:last-child{margin-bottom:0;}/* Used when elements stack in small viewports */
.services article{display:block; text-align:center; padding:20px}
.services article *{margin:0 0 15px 0;}
.services article > :last-child{margin-bottom:0;}
.services article .heading{font-size:1.2rem;}
#comments ul{margin:0 0 40px 0; padding:0; list-style:none;}
#comments li{margin:0 0 10px 0; padding:15px;}
#comments .avatar{float:right; margin:0 0 10px 10px; padding:3px; border:1px solid;}
#comments address{font-weight:bold;}
#comments time{font-size:smaller;}
#comments .comcont{display:block; margin:0; padding:0;}
#comments .comcont p{margin:10px 5px 10px 0; padding:0;}

#comments form{display:block; width:100%;}
#comments input, #comments textarea{width:100%; padding:10px; border:1px solid;}
#comments textarea{overflow:auto;}
#comments div{margin-bottom:15px;}
#comments input[type="submit"], #comments input[type="reset"]{display:inline-block; width:auto; min-width:150px; margin:0; padding:8px 5px; cursor:pointer;}
.container .sidebar{}

.sidebar .sdb_holder{margin-bottom:50px;}
.sidebar .sdb_holder:last-child{margin-bottom:0;}


#footer{padding:80px 0;}

#footer .heading{margin-bottom:50px; font-size:1.2rem;}

#footer .linklist li{display:block; margin-bottom:15px; padding:0 0 15px 0; border-bottom:1px solid;}
#footer .linklist li:last-child{margin:0; padding:0; border:none;}
#footer .linklist li::before, #footer .linklist li::after{display:table; content:"";}
#footer .linklist li, #footer .linklist li::after{clear:both;}

#footer .contact{}
#footer .contact.linklist li, #footer .contact.linklist li:last-child{position:relative; padding-left:40px;}
#footer .contact li *{margin:0; padding:0; line-height:1.6;}
#footer .contact li i{display:block; position:absolute; top:0; left:0; width:30px; font-size:16px; text-align:center;}

#footer input, #footer button{border:1px solid;}
#footer input{display:block; width:100%; padding:8px;}
#footer button{padding:8px 18px 10px; text-transform:uppercase; font-weight:700; cursor:pointer;}


#copyright{padding:20px 0;}
#copyright *{margin:0; padding:0;}


*, *::before, *::after{transition:all .28s ease-in-out;}
#mainav form *{transition:none !important;}

nav ul, nav ol{margin:0; padding:0; list-style:none;}

#mainav, #breadcrumb, .sidebar nav{line-height:normal;}
#mainav .drop::after, #mainav li li .drop::after, #breadcrumb li a::after, .sidebar nav a::after{position:absolute; font-family:"FontAwesome"; font-size:10px; line-height:10px;}
#mainav{}
#mainav ul{text-transform:uppercase;}
#mainav ul ul{z-index:9999; position:absolute; width:180px; text-transform:none;}
#mainav ul ul ul{left:180px; top:0;}
#mainav li{display:inline-block; position:relative; margin:0 15px 0 0; padding:0;}
#mainav li:last-child{margin-right:0;}
#mainav li li{width:100%; margin:0;}
#mainav li a{display:block; padding:30px 0;}
#mainav li li a{border:solid; border-width:0 0 1px 0;}
#mainav .drop{padding-left:15px;}
#mainav li li a, #mainav li li .drop{display:block; margin:0; padding:10px 15px;}
#mainav .drop::after, #mainav li li .drop::after{content:"\f0d7";}
#mainav .drop::after{top:35px; left:5px;}
#mainav li li .drop::after{top:15px; left:5px;}
#mainav ul ul{visibility:hidden; opacity:0;}
#mainav ul li:hover > ul{visibility:visible; opacity:1;}

#mainav form{display:none; margin:0; padding:0;}
#mainav form select, #mainav form select option{display:block; cursor:pointer; outline:none;}
#mainav form select{width:100%; padding:5px; border:none;}
#mainav form select option{margin:5px; padding:0; border:none;}
#breadcrumb{padding:120px 0 15px;}
#breadcrumb ul{margin:0; padding:0; list-style:none; text-transform:uppercase;}
#breadcrumb li{display:inline-block; margin:0 6px 0 0; padding:0;}
#breadcrumb li a{display:block; position:relative; margin:0; padding:0 12px 0 0; font-size:12px;}
#breadcrumb li a::after{top:3px; right:0; content:"\f101";}
#breadcrumb li:last-child a{margin:0; padding:0;}
#breadcrumb li:last-child a::after{display:none;}

.sidebar nav{display:block; width:100%;}
.sidebar nav li{margin:0 0 3px 0; padding:0;}
.sidebar nav a{display:block; position:relative; margin:0; padding:5px 10px 5px 15px; text-decoration:none; border:solid; border-width:0 0 1px 0;}
.sidebar nav a::after{top:9px; left:5px; content:"\f101";}
.sidebar nav ul ul a{padding-left:35px;}
.sidebar nav ul ul a::after{left:25px;}
.sidebar nav ul ul ul a{padding-left:55px;}
.sidebar nav ul ul ul a::after{left:45px;}
.pagination{display:block; width:100%; text-align:center; clear:both;}
.pagination li{display:inline-block; margin:0 2px 0 0;}
.pagination li:last-child{margin-right:0;}
.pagination a, .pagination strong{display:block; padding:8px 11px; border:1px solid; background-clip:padding-box; font-weight:normal;}

#backtotop{z-index:999; display:inline-block; position:fixed; visibility:hidden; bottom:20px; right:20px; width:36px; height:36px; line-height:36px; font-size:16px; text-align:center; opacity:.2;}
#backtotop i{display:block; width:100%; height:100%; line-height:inherit;}
#backtotop.visible{visibility:visible; opacity:.5;}
#backtotop:hover{opacity:1;}


table, th, td{border:1px solid; border-collapse:collapse; vertical-align:top;}
table, th{table-layout:auto;}
table{width:100%; margin-bottom:15px;}
th, td{padding:5px 8px;}
td{border-width:0 1px;}

#gallery{display:block; width:100%; margin-bottom:50px;}
#gallery figure figcaption{display:block; width:100%; clear:both;}
#gallery li{margin-bottom:30px;}


body{color:#CBCBCB; background-color:#1D1D1D;}
a{color:#FF8A00;}
a:active, a:focus{background:transparent;}/* IE10 + 11 Bugfix - prevents grey background */
hr, .borderedbox{border-color:#D7D7D7;}
label span{color:#FF0000; background-color:inherit;}
input:focus, textarea:focus, *:required:focus{border-color:#FF8A00;}

.overlay{color:#FFFFFF; background-color:inherit;}
.overlay::after{color:inherit; background-color:rgba(0,0,0,.55);}
.overlay.light{color:#474747;}
.overlay.light::after{background-color:rgba(255,255,255,.7);}

.btn, .btn.inverse:hover{color:#FFFFFF; background-color:#FF8A00; border-color:#FF8A00;}
.btn:hover, .btn.inverse{color:inherit; background-color:transparent; border-color:inherit;}

blockquote::before{color:rgba(255,255,255,.2);}

.icon{color:#FF8A00; border-color:#D7D7D7;}
a > .icon:hover, .services article:hover .icon{color:#FFFFFF; background-color:#FF8A00; border-color:#FF8A00;}

.row0, .row0 a{color:#474747; background-color:#EFEFEF;}
.row1{color:#474747; background-color:#FFFFFF; border-color:rgba(0,0,0,.1);}
.row2, .row2 a{}
.row3{color:#474747; background-color:#FFFFFF;}
.row4{color:#CBCBCB; background-color:#1D1D1D;}
.row5, .row5 a{color:#CBCBCB; background-color:#1D1D1D;}
.row5{border-color:rgba(255,255,255,.1);}


/* Top Bar */
#topbar ul li{border-color:rgba(0,0,0,.1);}
#topbar > div:last-of-type li:first-child a{color:#FF8A00;}


/* Header */
#header #logo a{color:inherit;}


/* Content Area */
.services article{box-shadow:0px 0px 8px rgba(0,0,0,.1);}
.services article:hover{background-color:rgba(0,0,0,.02);}


/* Footer */
#footer .heading{color:#FFFFFF;}
#footer hr, #footer .borderedbox, #footer .linklist li{border-color:rgba(255,255,255,.1);}

#footer input, #footer button{border-color:transparent;}
#footer input{color:#FFFFFF; background-color:#353535;}
#footer input:focus{border-color:#FF8A00;}
#footer button{color:#FFFFFF; background-color:#FF8A00;}


#mainav li a{color:inherit;}
#mainav .active a, #mainav a:hover, #mainav li:hover > a{color:#FF8A00; background-color:inherit;}
#mainav li li a, #mainav .active li a{color:#FFFFFF; background-color:rgba(0,0,0,.6); border-color:rgba(0,0,0,.6);}
#mainav li li:hover > a, #mainav .active .active > a{color:#FFFFFF; background-color:#FF8A00;}
#mainav form select{color:#FFFFFF; background-color:#FF8A00;}

#breadcrumb a{color:inherit; background-color:inherit;}
#breadcrumb li:last-child a{color:#FF8A00;}

.container .sidebar nav a{color:inherit; border-color:#D7D7D7;}
.container .sidebar nav a:hover{color:#FF8A00;}

.pagination a, .pagination strong{border-color:#D7D7D7;}
.pagination .current *{color:#FFFFFF; background-color:#FF8A00;}

#backtotop{color:#FFFFFF; background-color:#FF8A00;}

table, th, td, #comments .avatar, #comments input, #comments textarea{border-color:#D7D7D7;}
#comments input:focus, #comments textarea:focus, #comments *:required:focus{border-color:#FF8A00;}
th{color:#FFFFFF; background-color:#373737;}
tr, #comments li, #comments input[type="submit"], #comments input[type="reset"]{color:inherit; background-color:#FBFBFB;}
tr:nth-child(even), #comments li:nth-child(even){color:inherit; background-color:#F7F7F7;}
table a, #comments a{background-color:inherit;}

@-ms-viewport{width:device-width;}


@media screen and (min-width:978px){
	.hoc{max-width:978px;}
}

@media screen and (max-width:900px){
	.hoc{max-width:90%;}

	#topbar{}

	#header{padding:30px 0 15px;}
	#header #logo{margin:0;}

	#mainav{}
	#mainav ul{display:none;}
	#mainav form{display:block;}

	#breadcrumb{}

	.container{}
	#comments input[type="reset"]{margin-top:10px;}
	.pagination li{display:inline-block; margin:0 5px 5px 0;}

	#footer{}

	#copyright{}
	#copyright p:first-of-type{margin-bottom:10px;}
}


@media screen and (max-width:750px){
	.imgl, .imgr{display:inline-block; float:none; margin:0 0 10px 0;}
	.fl_left, .fl_right{display:block; float:none;}
	.group .group > *:last-child, .clear .clear > *:last-child, .clear .group > *:last-child, .group .clear > *:last-child{margin-bottom:0;}/* Experimental - Needs more testing in different situations, stops double margin when stacking */
	.one_half, .one_third, .two_third, .one_quarter, .two_quarter, .three_quarter{display:block; float:none; width:auto; margin:0 0 50px 0;}

	#topbar{padding-top:15px; text-align:center;}
	#topbar ul{line-height:normal;}
	#topbar div:first-child ul{margin-bottom:15px;}

	#header{text-align:center;}
	#header #logo{margin-bottom:15px;}

	.sectiontitle{max-width:none; text-align:left;}

	#footer{padding-bottom:50px;}/* Not Required, just looks better */
}


@media screen and (max-width:450px){
	#topbar ul li{margin-bottom:2px; padding-right:0; border-right:none;}
}


@media screen and (max-width:650px){
	.scrollable{display:block; width:100%; margin:0 0 30px 0; padding:0 0 15px 0; overflow:auto; overflow-x:scroll;}
	.scrollable table{margin:0; padding:0; white-space:nowrap;}

	.inline li{display:block; margin-bottom:10px;}
	.pushright li{margin-right:0;}

	.font-x2{font-size:1.4rem;}
	.font-x3{font-size:1.6rem;}

	#pageintro li article{max-width:none; width:100%;}
	#pageintro li .heading{font-size:1.6rem;}
}
</style>