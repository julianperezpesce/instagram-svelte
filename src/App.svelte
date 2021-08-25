<script>
  let username = '';
  let INSTA = 'https://instagram.com/'
  async function handleSearch(){
    let res = await fetch(INSTA + username + '?__a=1', {
      method: 'Get'
    });
    let data = await res.json();
    console.log(data);
  }
</script>

<main>
  <div class="header">
    <input type="text" bind:value={username}>
    <button on:click={handleSearch}>Search</button>
  </div>
</main>

<style>
  .header {
    padding: 30px 0px;
    align-items: center;
    justify-content: center;
    background: #111;
  }
</style>
