<script lang="ts">
  import { onMount } from "svelte";
  import axios from "axios";

  const endpoint = 'http://localhost:3000'

  interface FetchedItem{
    title: string
  };

  let suggestions: Array<FetchedItem> = [];
  
  onMount(async function () {
    try{
      console.log('mount')
      const response = await axios.get(endpoint);
      console.log(response.data);
      suggestions = response.data
    }catch(err){
      console.log(err)
    }
  });
</script>

<section>
  {#each suggestions as suggestion}
    <div>
      <p>{suggestion.title}</p>
    </div>
  {/each}
</section>