<script lang="ts">
  const handleClick = () => {
    document.cookie = "enthous_team=wilbertbocanegravelazquez; SameSite=None";
  };
</script>

<main>
  <button on:click={handleClick}>send</button>
</main>
