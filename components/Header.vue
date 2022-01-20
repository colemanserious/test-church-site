<template>
  <div id="hpc-header"
    class="header-bar relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0"
  >
	<b-navbar id="nav-bar" toggleable="sm" type="dark" variant="info">

		<b-collapse id="nav-collapse" is-nav>
		<b-navbar-brand href="/">
			<img class="logo" src="~/assets/HarundalePresLogo.png" />
			Harundale Presbyterian Church
		</b-navbar-brand>
			<b-navbar-nav>
				<b-nav-item href="/about">About</b-nav-item> 
				<b-nav-item href="/services">Services</b-nav-item>
				<b-nav-item href="/worship">Music</b-nav-item>
					
				<b-nav-item href="/learn">Learn</b-nav-item>
				<b-nav-item href="/serve">Serve</b-nav-item>
				<b-nav-item href="/contact">Contact</b-nav-item>
			</b-navbar-nav>
		</b-collapse>
		

		<b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
	</b-navbar>
  </div>
</template>

<script>
export default {
  name: 'HpcHeader',
}
</script>

<style>
	/**
        .header-bar {
		height: 15%;
		max-height: 500em;
        }
	**/

 	.logo { 
	 	height: 2em;
		border-radius: 50%;  /* round the image */
	}
</style>
