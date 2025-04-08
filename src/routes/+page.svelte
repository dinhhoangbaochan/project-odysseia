<script>
  import { onMount } from 'svelte';
  import { goto } from '$app/navigation';

  let initialized = false;

  onMount(() => {
    if (initialized) {
      goto('/dashboard');
    }
  });

  function startOdyssey() {
    goto('/dashboard');
  }
</script>

<main class="homepage">
  <h1 class="title">The Odysseia</h1>
  <p class="subtitle">
    Your personal journey of growth, memory, and mastery. Organize your learning paths, schedule reviews, and take notes — all in one elegant offline-first app.
  </p>

  <div class="cta-buttons">
    <button class="btn btn-primary" on:click={startOdyssey}>Start Your Odyssey</button>
    <button class="btn btn-secondary">Open Existing File</button>
  </div>
</main>

<style>
  .homepage {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: linear-gradient(to bottom right, #111, #222);
    color: white;
    padding: 2rem;
    font-family: 'Inter', sans-serif;
    text-align: center;
  }

  .title {
    font-size: 3rem;
    font-weight: bold;
    margin-bottom: 1rem;
  }

  .subtitle {
    font-size: 1.2rem;
    max-width: 600px;
    margin-bottom: 2rem;
    color: #ccc;
  }

  .cta-buttons {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  @media (min-width: 640px) {
    .cta-buttons {
      flex-direction: row;
    }
  }

  .btn {
    padding: 0.75rem 1.5rem;
    border: none;
    border-radius: 0.75rem;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
  }

  .btn-primary {
    background-color: #00c17c;
    color: white;
  }

  .btn-primary:hover {
    background-color: #00a969;
  }

  .btn-secondary {
    background-color: #444;
    color: white;
  }

  .btn-secondary:hover {
    background-color: #555;
  }
</style>