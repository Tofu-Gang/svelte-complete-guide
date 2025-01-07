<script>
    import Counter from "./lib/Counter.svelte";
    const counterProps = {
      initialCount: 3,
      maxCount: 6
    }
</script>
<Counter {...counterProps} />
<style>

</style>