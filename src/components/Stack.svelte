<script lang="ts">
  export let align: 'start' | 'center' | 'end' = 'start';
  export let justify: 'start' | 'center' | 'end' = 'start';
  export let gap: number = 0;
</script>

<div class="stack">
  <slot></slot>
</div>

<style>
  .stack {
    display: flex;
    flex-direction: column;
    align-items: {align};
    justify-content: {justify};
    gap: {gap}px;
  }
</style>

