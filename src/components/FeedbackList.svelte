<script>
  // import { onDestroy, onMount } from 'svelte';
  import { FeedbackStore } from '../stores';
  import { fade, scale } from 'svelte/transition';
  import FeedbackItem from './FeedbackItem.svelte';
  // let feedback = [];

  // onMount(() => {
  //   console.log('mounted');
  // });

  // onDestroy(() => {
  //   console.log('destroyed');
  // });
</script>

{#each $FeedbackStore as fb (fb.id)}
  <div in:scale={{ duration: 500 }} out:fade={{ duration: 500 }}>
    <FeedbackItem item={fb} />
    <!-- <FeedbackItem item={fb} on:delete-feedback /> -->
  </div>
{/each}
