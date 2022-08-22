<!-- a. Declaring props -->
<!-- b. Default values -->
<!-- App.svelte -->
<!-- <script>
	import Nested from './Nested.svelte';
</script>

<Nested answer={42}/>
<Nested/> -->

<!-- Nested.svelte -->

<!-- <script>
		export let answer = 'mystery';
</script>

<p>The answer is {answer}</p> -->

<!-- c. Spread props -->
<!-- App.svelte  -->
<script>
import Info from './Info.svelte';

	const pkg = {
		name: 'svelte',
		version: 3,
		speed: 'blazing',
		website: 'https://svelte.dev'
	};
</script>

<Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/>
<Info {...pkg}/>

<!-- Info.svelte  -->
<script>
	export let name;
	export let version;
	export let speed;
	export let website;
</script>

<p>
	The <code>{name}</code> package is {speed} fast.
	Download version {version} from <a href="https://www.npmjs.com/package/{name}">npm</a>
	and <a href={website}>learn more here</a>
</p>