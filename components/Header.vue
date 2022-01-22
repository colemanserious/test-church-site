<template>
  <div id="hpc-header"
    class="header-bar relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0"
  >
	<b-navbar id="nav-bar" toggleable="sm" type="dark" variant="info">

		<b-navbar-brand href="/">
			<img class="logo" src="~/assets/HarundalePresLogo.png" />
			Harundale Presbyterian Church
		</b-navbar-brand>

		<b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

		<b-collapse id="nav-collapse" is-nav>
			<b-navbar-nav>
				<b-nav-item href="/about">About</b-nav-item> 
				<b-nav-item href="/services">Worship</b-nav-item>
				<b-nav-item-dropdown text="Learn">
					<b-dropdown-item href="/learn/adults">Adult Sunday School</b-dropdown-item>
					<b-dropdown-item href="/learn/children">Children's Sunday School</b-dropdown-item>
					<b-dropdown-item href="/learn/youth">Youth</b-dropdown-item>
					<b-dropdown-item href="/learn/weekday">Weekday School</b-dropdown-item>
				</b-nav-item-dropdown>
				
				<b-nav-item-dropdown text="Serve">
					<b-dropdown-item href="/">Feeding the Hungry</b-dropdown-item>
					<b-dropdown-item href="/">Outreach</b-dropdown-item>
					<b-dropdown-item href="/">Mission</b-dropdown-item>
					<b-dropdown-item href="/">Stephen Ministry</b-dropdown-item>
				</b-nav-item-dropdown>
				<b-nav-item href="/contact">Contact</b-nav-item>
			</b-navbar-nav>
		</b-collapse>
		

	</b-navbar>
  </div>
</template>

<script>
export default {
  name: 'HpcHeader',
}
</script>

<style>
 	.logo { 
	 	height: 2em;
		border-radius: 50%;  /* round the image */
	}

	.dropdown-menu {
		border-radius: 0 1em 1em;
	}

</style>
