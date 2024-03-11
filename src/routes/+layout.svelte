<script>
	import '../app.pcss';
	import { browser } from '$app/environment';

	if (browser) {
		const theme = localStorage.getItem('theme');
		if (theme) {
			document.documentElement.setAttribute('data-theme', theme);
		} else {
			localStorage.setItem('theme', 'dark');
			document.documentElement.setAttribute('data-theme', 'dark');
		}
	}
</script>
<!-- svelte-ignore a11y-missing-attribute -->
<html class="bg-math">
</html>
<slot />
