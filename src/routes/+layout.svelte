<script>
    import "../app.css";
    import Navbar from '../components/Navbar.svelte';
</script>

<svelte:head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css">
</svelte:head>
  
<Navbar />
  
<slot />