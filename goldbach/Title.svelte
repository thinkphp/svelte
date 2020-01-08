<script>
	export let name;
	export let version;
	export let speed;
	export let website;
	export let doit;
</script>

<style>
	h1 {
		 color: orange;
		 font-size: 50px;
		 font-family: Arial;
	}
	h3 {font-family: Verdana; color: green} 
</style>

<h1>Goldbach's conjecture</h1>
<p>
	The <code>{name}</code> package is {speed} fast.
	Download version {version} from <a href="http://{doit}.ro">npm</a>
	and <a href={website}>learn more here</a>
</p>

<h3>Every even integer greater than 2 can be expressed as the sum of two primes.</h3>
