<script>
    let apiResponse = 'placeholder';

    async function getApiResponse() {
        const response = await fetch('http://localhost:3000');
        const x = await response.json()
        apiResponse = x.message.message.content;
    }
</script>

<h1 class="m-10">Welcome to SvelteKit, Fred</h1>
<button class="border-4 rounded-xl p-4 bg-blue-600" on:click={getApiResponse}>Click Me for API Magic</button>
<div>{apiResponse}</div>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
