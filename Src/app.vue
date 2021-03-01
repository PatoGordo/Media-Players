const app = new Vue({
	router, //router from Src/router.js
	el: "#app",
	data: {

	},
	template: `
		<div id="app">
			<router-view></router-view>
			<app-navbar /><!-- Component from: Src/Components/navbar.vue.js -->
		</div>
	`
}).$mount("#app")