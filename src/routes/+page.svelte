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


</script>

<div class="center">
<h1>Hello {name}</h1>
<h2>I {isHired} work in {@html company}</h2>


<button on:click={() => disabled = !disabled}>Toggle</button>
<br />
<button on:click={() => disabled = true}>Dont let me buy vimal</button>
<br />

<button on:click={() => disabled = false}>let me buy vimal</button>

<br />




<button {disabled} on:click={() => alert("I am clicked")}>Buy vimal</button>

<br />

<Button />
</div>


<style>
    h1 {
        color: goldenrod;
        font-family: "Comic Sans MS", cursive, sans-serif;
        font-size: 2rem;
    }


    .center {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }
</style>
