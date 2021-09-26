<template>
	<div id="app" v-scroll="fader">
		<Header />
		<b-container
			id="stuff-container"
			class="py-2 shadows-second"
			:style="{ opacity: stuffOpacity }"
			fluid
		>
			<b-container fluid class="filter py-2">
				<About class="mt-3" />
				<Work />
				<Socials />
			</b-container>
		</b-container>
	</div>
</template>

<script>
import Header from "@/components/Header.vue";
import Work from "@/components/Work.vue";
import About from "@/components/About.vue";
import Socials from "@/components/Socials.vue";

export default {
	name: "App",
	data() {
		return {
			stuffOpacity: 50,
		};
	},
	components: {
		Header,
		Work,
		About,
		Socials,
	},
	created() {},
	destroyed() {
		document.addEventListener("scroll", this.fader());
	},
	methods: {
		fader() {
			//do something
			//scrollly boy really cool effect
			console.log(window.scrollY);
			this.stuffOpacity = window.scrollY / 500;
		},
	},
	directives: {
		scroll: {
			// do
			inserted: function(el, binding) {
				let f = function(evt) {
					if (binding.value(evt, el)) {
						window.removeEventListener("scroll", f);
					}
				};
				window.addEventListener("scroll", f);
			},
		},
	},
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap");
html body {
	background-image: url("~@/assets/mountain.jpg");
	background-size: cover;
	background-attachment: fixed;
}
#app {
	font-family: "Lato", sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #282a3d;
}
#stuff-container {

	background: linear-gradient(90deg, #141E30 0%, #243B55 100%);

	background-size: cover;
	z-index: 2 !important;
}
.container {
	border-radius: 0.3em;
}
.bg-main {
	background-color: #e9e9e0 !important;
	opacity: 0.8;
	backdrop-filter: saturate(180%) blur(0.5em) hue-rotate(90deg);
}
.bg-second {
	background-color: #080c18 !important;
	color: #ffff0f;
	opacity: 0.8;
	backdrop-filter: saturate(140%) blur(0.5em) hue-rotate(120deg);
}
.shadows-main {
	box-shadow: 9px 9px 16px rgb(40, 42, 61, 0.9),
		-9px -9px 16px rgba(233, 233, 224, 0.3);
}
.shadows-second {
	box-shadow: 9px 9px 16px rgb(40, 42, 61, 0.6),
		-9px -9px 16px rgba(233, 233, 224, 0.2);
}
</style>
