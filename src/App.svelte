<script>
  import Footer from './lib/footer.svelte'
  import MainContent from './lib/main-content.svelte'
</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link
    rel="preconnect"
    href="https://fonts.gstatic.com"
    crossorigin="anonymous"
  />
  <link
    href="https://fonts.googleapis.com/css2?family=Manrope:wght@500;700&display=swap"
    rel="stylesheet"
  />
</svelte:head>

<div
  class="min-h-screen flex flex-col bg-cstm-light-grayish-blue px-5 pt-20 font-manrope"
>
  <MainContent />
  <Footer />
</div>
