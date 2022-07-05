<script lang="ts">
  const handleClick = () => {
    document.cookie = "enthous_team=wilbertbocanegravelazquez;samesite=none";
  };
</script>

<main>
  <button on:click={handleClick}>send</button>
</main>
