<template>
<div class="easteregg-container">
	<img ref="easteregg" src="src/components/EasterEgg/toasty.png" alt="Toasty" class="easteregg">
	<audio ref="audio" src="src/components/EasterEgg/toasty.mp3"></audio>
</div>
</template>

<script>
export default {
	mounted: function() {
		var that = this;
		cheet('↑ ↑ ↓ ↓ ← → ← → b a', function () {
			var e = that.$refs.easteregg;
			var active = "active";
			var timeout = 1000;
			var audio = that.$refs.audio;

			if (!e.classList.contains(active)) {
				e.classList.add(active);
				audio.play();

				setTimeout(function() {
					e.classList.remove(active);
				}, timeout);
			}
		});
	}
}
</script>

<style lang="sass">

.easteregg-container {
	position: fixed;
	right: 0;
	bottom: 0;
	overflow: hidden;
	z-index: 999;
	pointer-events: none;

	.easteregg {
		transform:translate(100%, 0);
		transition: transform 0.3s;

		&.active {
			transform:translate(0, 0);
		}
	}
}

</style>