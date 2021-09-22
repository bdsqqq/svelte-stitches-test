<script>
	import { css } from "@stitches/core";
	let count = 0;

	function handleClick() {
	  count += 1;
	}

	const button = css({
	  background: "gray",
	  color: "white",
	  border: "none",
	  padding: "8px 12px",
	  borderRadius: "2px",

	  "@media screen and (prefers-reduced-motion: no-preference)": {
	    transitionTimingFunction: "cubic-bezier(0.2, 0, 0.38, 0.9)",
	    transitionDuration: "70ms"
	  },

	  "&:hover": {
	    background: "black"
	  }
	});
</script>

<button class={button()} on:click={handleClick}>
  Clicked {count} {count === 1 ? 'time' : 'times'}
</button>