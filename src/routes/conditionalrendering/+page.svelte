<script>
    let value = 0;
</script>

<section>

<input type="number" on:change={

    (event) => {
        value = event.target.value;
        if (value > 1000000) {
        alert('Too big!');
        }
    }
}>

<h1>{value}</h1>



{#if value%2 === 0}
    <p>This is even number</p>
{:else if value%2 != 0}
    <p>Thats a odd number</p>
{:else}
    <p>Extrenal server error</p>
{/if}


</section>


<style>
    section {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        height: 100vh;
    }
</style>




