<script>
  let user = '';
  function lengthValid(string) {
    if (string.length > 0) {
      window.location.href = '/users/' + string;
    }
  }
  function onKeyPress(e) {
    if (e.charCode === 13) lengthValid(user);
  }
</script>

<h1 class="text-3xl font-bold mb-2">Welcome to Scratchinfo!</h1>
<p>
  This is a small project. You can use the search bar down below to search for a Scratch user, and
  it will return some information.
</p>
<p>
  This website runs on <a href="https://svelte.dev">Svelte</a> and
  <a href="https://kit.svelte.dev">SvelteKit</a> which are both epic projects.
</p>
<input
  placeholder="Search a User"
  type="text"
  class="p-2 text-black rounded pl-3"
  id="user"
  on:keypress={onKeyPress}
  bind:value={user}
/>
<button class="btn-primary" on:click|preventDefault={() => lengthValid(user)}>search</button>
<br />
<a href="/privacy" class="hover:underline hover:font-semibold transition-all">Privacy Policy</a>
<br />
<a href="/rules" class="hover:underline hover:font-semibold transition-all"
  >Rules for using Scratchinfo</a
>

<!-- <style>
  input {
    border: 2px black;
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
    padding-left: 10px;
    width: 30em;
  }
</style> -->
