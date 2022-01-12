<script>
  let visibility = 'hidden'

  const toggleVisibility = () => {
    visibility = visibility === 'hidden' ? 'visible' : 'hidden'
  }
</script>

<main class="flex-1">
  <div class="bg-white rounded-xl relative">
    <img src="/assets/drawers.jpg" alt="drawers" class="rounded-t-xl" />
    <div class="px-10 py-8 text-cstm-dark-grayish-blue">
      <h1 class="font-bold mb-3">
        Shift the overall look and feel by adding these wonderful touches to
        furniture in your home
      </h1>
      <p>
        Ever been in a room and felt like something was missing? Perhaps it felt
        slightly bare and uninviting. I’ve got some simple tips to help you make
        any room feel complete.
      </p>
      <div class="flex justify-between items-center mt-12">
        <div class="flex items-center gap-5">
          <img
            src="/assets/avatar-michelle.jpg"
            alt="michelle's avatar"
            class="w-10 rounded-full"
          />
          <div>
            <p>Michelle Appleton</p>
            <p>28 Jun 2020</p>
          </div>
        </div>
        <button
          class="bg-cstm-light-grayish-blue p-2 rounded-full"
          on:click={toggleVisibility}
        >
          <img src="/assets/icon-share.svg" alt="share" />
        </button>
      </div>
    </div>
    <div
      class={`bg-cstm-dark-grayish-blue text-cstm-grayish-blue px-10 py-9 rounded-b-xl absolute bottom-0 w-full ${visibility}`}
    >
      <div class="flex justify-between items-center">
        <div class="flex items-center gap-5">
          <p class="uppercase tracking-[0.4em]">Share</p>
          <div class="flex items-center gap-5">
            <img src="/assets/icon-facebook.svg" alt="facebook icon" />
            <img src="/assets/icon-twitter.svg" alt="twitter icon" />
            <img src="/assets/icon-pinterest.svg" alt="pinterest icon" />
          </div>
        </div>
        <button
          class="bg-cstm-desaturated-dark-blue p-2 w-fit rounded-full"
          on:click={toggleVisibility}
        >
          <img src="/assets/icon-share-white.svg" alt="share" />
        </button>
      </div>
    </div>
  </div>
</main>
