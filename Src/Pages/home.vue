const Home = Vue.component('Home', {
  data: function () {
    return {
			giant: "HOME",
  		title: "VueRouter CDN Template with Less - Home",
			visibility: false,
			audioData: [],
			current: 0,
			audioQuntity: 0
    }
  },
	methods:{
		
		changeTheme(){
			document.body.classList.toggle('dark')
		}
	},
	created(){
		document.title = this.title
		
	  this.audioData =	window.audios
		this.audioQuntity = this.audioData.length
		this.current = 1
	},
  template: `
	<div class="component home">
		<h2 @click="changeTheme">Audio</h2>
		<div class="player" v-for="item in audioData.slice(current-1,current)">
			<h4><ion-icon name="podium-sharp"></ion-icon> Duck Player</h4>
			<div class="card">
				<div class="card-image" :style="'background-image: url(Src/assets/images/'+ item.cover +')'">
					<a href="#" class="btn-floating btn-large halfway-fab">
            
          </a>
				</div>
				<div class="card-content">
					<h5 class="card-title">{{item.title}}</h5>
					<p class="card-artist">{{item.artist}}</p>
					<!--audio :src="'Src/assets/audios/'+ item.file "></audio-->
				</div>
			</div>
		</div>
		<button @click="current--" :style="current <= 1 ? 'display: none;' : 'display: block;'">Back</button>
		<button @click="current++" :style="current >= audioQuntity ? 'display: none;' : 'display: block;'">Next</button>
	</div>`
})