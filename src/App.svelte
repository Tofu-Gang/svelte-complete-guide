<script>
  const name = "Svelte";
  const lorem_picsum_src = "https://picsum.photos/200";
  const string = "Some <strong>string</strong> with html.";
</script>

<img src={lorem_picsum_src} alt="Some text {name.toLowerCase()}" />
<h1>Hello {name.toUpperCase()}!</h1>
<p>{@html string}</p>

<style>
  h1 {
    color: red;
  }
</style>