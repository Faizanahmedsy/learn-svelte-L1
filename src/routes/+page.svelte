<script>

    import Button from "../components/Button.svelte"

    let name = "Faizan"

    let company = "<i>Google</i>"


    let knowDsa = false
 
    let isHired;

    if(knowDsa) {
         isHired = "do"
    } else {
         isHired = "do not"
    }


    let disabled = false

    let     disClass = "text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800"


    if (disabled){
        disClass = "text-white bg-red-400 dark:bg-red-500 cursor-not-allowed font-medium rounded-lg text-sm px-5 py-2.5 text-center"
    } else {
        disClass= "text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800"
    }






</script>

<div class="flex flex-col justify-center items-center h-screen">
<h1 class="text-4xl text-orange-300 font-bold p-4">Hello {name}</h1>
<h2>I {isHired} work in {@html company}</h2>





<button on:click={() => disabled = !disabled}>Toggle</button>
<br />
<button on:click={() => disabled = true} class="text-white bg-red-700 hover:bg-red-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-red-600 dark:hover:bg-red-700 focus:outline-none dark:focus:ring-red-800">Dont let me buy vimal</button>
<br />

<button on:click={() => disabled = false} class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800">let me buy vimal</button>

<br />




<button {disabled} on:click={() => alert("Bolo zuba kesri")} class={disabled ? "text-white bg-zinc-400 dark:bg-zinc-500 cursor-not-allowed font-medium rounded-lg text-sm px-5 py-2.5 text-center" : "text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5  dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800"}>Buy vimal</button>

<br />

<Button />
</div>


<style>
    /* h1 {
        color: goldenrod;
        font-family: "Comic Sans MS", cursive, sans-serif;
        font-size: 2rem;
    } */

 
    /* .center {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
    } */
</style>
