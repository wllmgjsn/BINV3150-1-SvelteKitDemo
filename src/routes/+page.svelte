<script>
  import '#lib/style.css';
  let { data } = $props();

  let compteur = $state(0);

  function incrementer() {
    compteur++;
  }
</script>

<main class="demo">

  <h1>Hello World !</h1>
  <p>{data.message}</p>

  <button onclick={incrementer}>
    Nombre de clics : {compteur}
  </button>
</main>