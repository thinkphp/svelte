<script>
	import Title from './Title.svelte';
	import Footer from './Footer.svelte';
	
	 const pkg = {
		name: 'svelte',
		version: 3,
		speed: 'very',
		doit: 'thinkphp',
		website: 'http://thinkphp.github.com'
	};
	
	let a = 2;
	let out = ""
	
	function isPrime(n) {
		
		       var prime = 1;
		
		       if(n == 1 || n == 0) return false;		        
		
		       for(i = 2; i <= Math.sqrt(n) && prime; i++) {
						 
						       prime = ((n % i) != 0)
					 } 		
		     return prime;
	} 
	
	function handlerClick() {
		
		       alert(Math.sqrt(a))
	}
	
		function handlerKeyUp() {
		       
	 	       var i = 2;
		
		       out = ""
		
		       while(i <= a / 2) {
					 
						     if(isPrime(i) && isPrime(a - i)) {
									 
									  out += a + " = "+ i + ' + ' + (a - i) + "<br/>";
								 } 
						     i++;
  				 } 
	}
</script>

<style>
	button {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
	
	p {
		 font-size: 40px; 
		 color: violet
	}
</style>

<Title name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website} doit={pkg.doit}/>

<input type="numeric" bind:value="{a}" on:keyup="{handlerKeyUp}"/>
<button on:click="{handlerClick}">Goldbach</button>
<p>{@html out}</p>

<Footer />
