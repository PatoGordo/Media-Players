Vue.component('app-navbar', {
  data: function () {
    return {

    }		
  },
	methods:{
		
	},
  template: `
	<p class="navbar">
		<router-link to="/" class="navbar-item"><ion-icon name="musical-notes-outline"></ion-icon></router-link>
		<router-link to="/video" class="navbar-item"><ion-icon name="videocam-outline"></ion-icon></router-link>
	</p>
	`
})