<script>
	export let name;
	export let version;
	export let speed;
	export let website;
	export let doit;
</script>

<style>
	h1 {
		 color: #7FFFD4;
		 font-size: 50px;
		 font-family: Arial;
	}
	h3 {font-family: Verdana; 
		  color: #8FBC8F;
	    } 
</style>

<h1>Fundamental Theorem of Arithmetic</h1>
<p>
	The <code>{name}</code> package is {speed} fast.
	Download version {version} from <a href="http://{doit}.ro">npm</a>
	and <a href={website}>learn more here</a>
</p>

<h3>In Number Theory unique factorization theorem states that every integer greater than 1 either is a prime number itself or can be represented as the product of prime numbers</h3>
