<script lang="ts">
  import { onMount } from "svelte";
  import logo from "./assets/svelte.png";
  import Counter from "./lib/Counter.svelte";

  const handleClick = async () => {
    const req = await fetch("http://localhost:3000/auth/login", {
      method: "POST",
      credentials: "include",
    });

    const res = await req.json();

    console.log(res);
  };

  const handleGetCookie = () => {
    console.log(document.cookie);
  };

  const handleRemoveCookie = async () => {
    const req = await fetch("http://localhost:3000/auth/remove", {
      method: "PUT",
      credentials: "include",
    });

    const res = await req.json();
    console.log(res);
  };

  $: console.log("simon", document.cookie);
</script>

<main>
  <button on:click={handleClick}>send</button>
  <button on:click={handleGetCookie}>get</button>
  <button on:click={handleRemoveCookie}>remove</button>
</main>
