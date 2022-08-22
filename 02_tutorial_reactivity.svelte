<!-- a. Assignments -->
<!-- <script>
	let count = 0;

	function incrementCount() {
		count += 1;
	}
</script>

<button on:click={incrementCount}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>  -->

<!-- b. Declarations -->
<!-- <script>
	let count = 0;
	$: doubled = count * 2;

	function handleClick() {
		count += 1;
	}
</script>

<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p>{count} doubled is {doubled}</p> -->

<!-- c. Statements -->
<!-- <script>
	let count = 0;

	$: if (count >= 10) {
		alert('count is dangerously high!');
		count = 9;
	}
  $: {
    console.log('the count is ' + count);
    console.log('hello');
  }

	function handleClick() {
		count += 1;
	}
</script>

<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button> -->

<!-- d. Updating arrays and objects -->
<script>
	let numbers = [1, 2, 3, 4];
	function addNumber() {
		// 1
		// numbers.push(numbers.length + 1);
		// numbers = numbers;
		// 2
		// numbers = [...numbers, numbers.length + 1];
		// 3
		numbers[numbers.length] = numbers.length + 1;
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>