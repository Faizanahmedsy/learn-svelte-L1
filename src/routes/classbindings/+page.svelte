<script>
    let italise = true;


    let makeItItalic = true
</script>

<h2>I know</h2>

<!-- This is a regluat way of conditionally applying classnames -->
<p class={italise ? "italise" : " "}>Java</p>


<!-- SPECIAL SVELTE DIRECTIVES -->

<!-- if the condition is based on a variable with different name use this syntax -->
<p class:italise={makeItItalic} >Javascript</p>


<!-- if the classsname and variable name are same then use this syntax -->
<p class:italise>Next jS</p>

<p>C</p>


<style>
   .italise {
        font-style: italic;
    }
</style>