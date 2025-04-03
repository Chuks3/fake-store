<template>
  <div class="navbar">
		<router-link to="/">SHOPPING APP</router-link>
</div>
</template>

<style scoped>
.navbar {
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
	height: 50px;
	display: flex;
	align-items: center;
	justify-content: center;
	box-shadow: 0px 5px 15px 5px rgba(0, 0, 0, 0.35);
	background-color: #282c34;
	z-index: 9;
}

.navbar a {
	font-family: "Montserrat", sans-serif;
	font-weight: 800;
	font-size: xx-large;
	color: #3bb99b;
	text-decoration: none;
}
</style>
