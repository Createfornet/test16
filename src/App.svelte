
<script lang="ts">
  import './app.css'
  import Header from "./components/Header.svelte";
  import SectionSuggestions from './components/SectionSuggestions.svelte';
  import TopNews from './components/TopNews.svelte';
  let num: number = 3

  
</script>

<main class="m-4 p-2 border">
  <Header/>
  <TopNews/>
  <SectionSuggestions/>
</main>
