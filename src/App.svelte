<script>
  let username = '';
  let INSTA = "https://instagram.com/";
  async function searchUser(){
		let res = await fetch(INSTA+username+"?__a=1",{
      mode: "no-cors",
      headers: {"Access-Control-Allow-Origin": "*"},
			method:"GET"
		});
		let data = await res.json();
		console.log(data);
  }
</script>

<main>
  <div class="header">
    <input type="text" bind:value={username}>
    <button on:click={searchUser}>Search</button>
  </div>
</main>

<style>
  .header {
    padding: 10px 0px;
    text-align: center;
    justify-content: center;
    background: #111;
  }
</style>
