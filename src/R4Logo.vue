<template>
	<svg :class="layoutClass" width="150" height="130" viewBox="0 0 150 130" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:figma="http://www.figma.com/figma/ns"><title>Radio4000</title><g figma:type="frame" fill="#FFF"><use xlink:href="#a" transform="translate(62.367 18.91)" figma:type="vector-operation"/><use xlink:href="#b" figma:type="vector-operation"/></g><defs><path id="a" fill-rule="evenodd" d="M54.51 89.487H0v-19.92L42.15 0h32.486v69.724H87.63v19.763H74.636v21.187H54.51V89.487zm5.866-53.654l-28.71 40h28.99v-40h-.28z"/><path id="b" fill-rule="evenodd" d="M7.818 91.806H0V0h40.76c23.284 0 37.878 8.13 37.878 26.624 0 16-12.626 24.132-29.516 26.1l25.91 39.082h-12.3L37.645 54.38H7.818v37.426zM7.59 25.248v21.05h27.14c12.387 0 23.66-2.438 23.66-10.49 0-8.05-10.3-10.56-23.938-10.56H7.592z"/></defs></svg>
</template>

<script>
	export default {
		name: 'r4-logo',
		props: {
			isOnline: Boolean
		},
		computed: {
			layoutClass() {
				if (this.isOnline) {
					return 'R4 R4--isOnline'
				} else {
					return 'R4 R4--isOffline'
				}
			}
		}
	}
</script>

<style scoped>
	.R4 {
		width: 1.2em;
		height: 1.2em;
		/*fill: white;*/
		fill: black;
	}
	.R4 * {
		fill: inherit;
	}
	.R4--isOffline {
		fill: #5e1ae6;
	}
</style>
