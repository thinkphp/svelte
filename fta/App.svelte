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
	
	function handlerKeyUp() {		          
		
		                    out = ""   
		
		                    var n = parseInt(a),

                        fm , i = 2;                        
		
		                    if(a == "") return;

                        out += n + " = "

                        var str = "";

                        do {

                            fm = 0;

                             while(n % i == 0) {

                                fm = fm + 1;

                                n = parseInt(n / i)
                             }

                             if(fm!=0) str += i + "^" + fm + " * ";

                             i = i + 1;   

                        } while(n != 1)

                        str = str.slice(0, -2);

                        out += str +  "<hr/>"                    
	}
	
  function handlerClick() {
		       
	 	       var EPS = 0.00001

             var an, 
                 anplus1, n = parseInt(a);

                 an = parseFloat(n / 2.0); 

                 anplus1 = ( an + parseFloat ( n / an)  ) / 2.0  

                 while( (anplus1 > an ? anplus1 - an : an - anplus1) >= EPS ) {

                        an = anplus1

                        anplus1 = ( an + parseFloat( n / an) ) / 2  
                 }
           
           alert("sqrt(" + n + ") = " + anplus1)
	}
</script>

<style>
	button {
  background-color: green; /* Green */
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
		 color: orange
	}
</style>

<Title name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website} doit={pkg.doit}/>

<input type="numeric" bind:value="{a}" on:keyup="{handlerKeyUp}"/>
<button on:click="{handlerClick}">SQRT</button>
<p>{@html out}</p>

<Footer />
