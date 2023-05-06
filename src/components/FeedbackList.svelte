<script>
  import { fade, scale } from "svelte/transition";
  import FeedbackItem from "./FeedbackItem.svelte";

  export let feedback = [];
</script>

{#each feedback as fb (fb.id)}
  <div in:scale out:fade={{ duration: 400 }}>
    <FeedbackItem item={fb} on:delete-item />
  </div>
{/each}
