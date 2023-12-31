<script>
    //This are initial states
    let value = 0
    let name = ["Vimal", "Kumar", "Singh"]


    let fullNames = [
        {firstName: "Vimal", lastName: "Patel"},
        {firstName: "Kumar", lastName: "Singh"},
        {firstName: "Jaydeep", lastName: "Kumar"}
    ]


    function handleChange (event) {
        value = event.target.value;
        if (value > 1000000) {
        alert('Too big!');
        }
    }
</script>

<section>
<input type="number" on:change={handleChange}/>
<h1>{value}</h1>

<!-- conditional rendering by svelte special if else blocks -->
{#if value%2 === 0}
    <p>This is even number</p>
{:else if value % 2 !== 0}
    <p>Thats a odd number</p>
{:else}
    <p>Extrenal server error</p>
{/if}



<!-- iterating over an array  -->
<div>
    {#each name as item, index}
        <h2 >{index + 1} {item}</h2>
    {/each}
</div>

<div>
    {#each fullNames as item,index}
    <h2>{index+ 1} {item.firstName} {item.lastName}</h2>
    {/each}
</div>

</section>




<!-- //This is the css for this page -->
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




