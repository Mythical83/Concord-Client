<script>
  import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

  function messageHandler() {
    dispatch('message', {
      text: 'test'
    });
  }
</script>

<main>
  
</main>

<style>

</style>