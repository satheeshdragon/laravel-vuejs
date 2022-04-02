

<template>
	<div>
		<Header />

		<div id="wrapper">
<br>
			<div id="content-wrapper">
				<router-view></router-view> <!-- container-fluid div Replaced by router-view -->

				<Footer />
			</div>
		</div>
	</div>
</template>

<script>
    import Header from './components/Header.vue';
    import Footer from './components/Footer.vue';

    export default{
        components:{
            Header,
            Footer
        },
	created() {
		document.querySelector("body").style.backgroundColor = "#fff";
	}
    }
</script>