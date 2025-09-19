<h1>Welcome to the weather page</h1>
<nav>
    <a href="/">Home</a>
    <a href="/24hour">24-Hours</a>
    <a href="/7days">7 days</a>
</nav>

<button on:click={myFunction}>Toggle dark mode</button>

<script>
function myFunction() {
   var element = document.body;
   element.classList.toggle("dark-mode");
}
</script>