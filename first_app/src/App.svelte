<!-- c. Spread props -->

<script>
	import Tutorial from '../../03_tutorial.svelte';
import Info from './Info.svelte';
import Nested from './Nested.svelte';

	const pkg = {
		name: 'svelte',
		version: 3,
		speed: 'blazing',
		website: 'https://svelte.dev'
	};
</script>

<Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/>
<Info {...pkg}/>