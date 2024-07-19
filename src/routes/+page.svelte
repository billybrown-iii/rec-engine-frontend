<script>
    // consider daisyUI for component library

    let apiResponse = 'placeholder';

    async function getApiResponse() {
        const response = await fetch('http://localhost:3000');
        const x = await response.json()
        apiResponse = x.message.message.content;
    }
</script>

<button class="border-4 rounded-xl p-4 bg-blue-600" on:click={getApiResponse}>Click Me for API Magic</button>
<div>{apiResponse}</div>

<hr class='my-10'>

<div>Welcome to home page</div>


