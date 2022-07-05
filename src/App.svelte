<script lang="ts">
  const handleClick = () => {
    document.cookie = "enthous_team=again; SameSite=None; Secure";
  };
</script>

<main>
  <button on:click={handleClick}>send</button>
</main>
