<script lang="ts">
  import Content from './lib/Content.svelte';
  import { onMount } from 'svelte';

  let isDarkMode = false;

  onMount(() => {
    const savedTheme = localStorage.getItem('theme');
    isDarkMode = savedTheme === 'dark' || 
      (!savedTheme && window.matchMedia('(prefers-color-scheme: dark)').matches);
    updateTheme();
  });

  function toggleTheme() {
    isDarkMode = !isDarkMode;
    updateTheme();
  }

  function updateTheme() {
    document.documentElement.classList.toggle('dark-mode', isDarkMode);
    localStorage.setItem('theme', isDarkMode ? 'dark' : 'light');
  }
</script>

<main>
  <button class="theme-toggle" on:click={toggleTheme}>
    {isDarkMode ? '☀️' : '🌙'}
  </button>
  <Content />
</main>

<style>
  :global(body) {
    margin: 0;
    padding: 0;
    min-height: 100vh;
    transition: background-color 0.3s ease, color 0.3s ease;
  }

  main {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding: 2rem;
  }

  .theme-toggle {
    position: fixed;
    top: 1rem;
    right: 1rem;
    padding: 0.5rem;
    font-size: 1.5rem;
    border: none;
    background: none;
    cursor: pointer;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
