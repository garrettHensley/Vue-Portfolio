<template>
	<div id="socials-container">
		<div class="d-flex justify-content-around align-items-center text-dark">
			<span class="" v-for="link in links" :key="link.id">
				<b-button :href="link.href" target="_blank" :key="link.name">
					<span>{{ link.name }}</span>
				</b-button>
			</span>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			links: [
				{ name: "GitHub", href: "https://github.com/garrettHensley" },
				{ name: "Resume", href: "http://garretthensley.me/resume.html" },
				{ name: "Email", href: "mailto:garrettmichaelhensley@gmail.com" },
			],
		};
	},
};
</script>

<style scoped>
.avatar {
	background-color: #e9e9e0;
	border-radius: 50%;
	border: 0.1rem solid #e9e9e0;
	box-shadow: 0.2rem 0.2rem 16px rgb(40, 42, 61, 0.6),
		-0.2rem -0.2rem 16px rgba(233, 233, 224, 0.7);
}

.fixed {
	position: absolute;
	top: 19em;
	left: 75em;
	z-index: 2;
}
.btn {
	display: flex;
	color: black;
	background: #ddeeeb !important;
	align-items: center;
	justify-content: center;
	height: 5em;
	width: 5em;
	border-radius: 50%;
	border: white;
	box-shadow: -10px -10px 20px 0px rgb(224, 216, 216),
		5px 5px 20px 0px rgb(68, 67, 67);
}
</style>
