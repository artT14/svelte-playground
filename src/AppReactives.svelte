<script>
	let firstName = 'Bruce'
	let lastName = 'Willis'
	$:fullName = `${firstName} ${lastName}` //reactive decleration
											// updates automatically when their dependancies change

	let items = [
		{
			id: 1,
			title: 'TV',
			price: 100
		},
		{
			id: 2,
			title: 'Blender',
			price: 50
		},
		{
			id: 3,
			title: 'Laptop',
			price: 300
		},
	]
	$:total = items.reduce((total,curr)=>(total += curr.price),0)
	$: {
		console.log(`Full Name is ${firstName} ${lastName}`)
		console.log(`Total is ${total}`)
	} //reactive statement, when firstName||lastName||total changes, we run this block

	let volume = 0
	$: if(volume < 0){
		alert("Can't go any lower than 0")
		volume = 0
	} else if(volume > 20){
		alert("Can't go any higher than 20")
		volume = 20
	}
</script>

<main>
	<h2>Current Volume: {volume}</h2>
	<button on:click={()=>(volume += 2)}>Increase Volume</button>
	<button on:click={()=>(volume -= 2)}>Decrease Volume</button>
	<button on:click={()=>{
		firstName = 'Clark'
		lastName = 'Kent'
	}}>Change Name</button>
	<h2>{firstName} {lastName}</h2>
	<h2>{fullName}</h2>
	<h2>
		Total - {total}
	</h2>
	<button on:click={()=>(items = [...items,{id:4,title:'Mouse',price:20}])}>Add Item</button>
</main>

<style>
	main {
		/* text-align: center; */
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>