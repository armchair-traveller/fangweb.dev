<!-- Layout is for any layout components like Nav. 
  Similar to layout in Gatsby, present on all pages -->
<script>
  import Header from "$components/Header.svelte";
  import "./_global.pcss";
</script>

<Header />
<slot />
