<script>
  import { slide } from 'svelte/transition'

  let visibility = 'hidden'
  let isVisible = false

  const toggleVisibility = () => {
    visibility = visibility === 'hidden' ? 'block' : 'hidden'
    isVisible = !isVisible
  }
</script>

<main class="flex-1 flex flex-col justify-center">
  <div
    class="bg-white rounded-xl relative md:flex md:items-center md:max-w-5xl md:mx-auto"
  >
    <img
      src="/assets/drawers.jpg"
      alt="drawers"
      class="w-full rounded-t-xl md:rounded-none md:rounded-l-xl md:max-w-md"
    />
    <div class="px-10 py-8 text-cstm-dark-grayish-blue">
      <h1 class="font-bold mb-3 md:text-2xl">
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
        <div>
          <button
            class="bg-cstm-light-grayish-blue p-2 rounded-full peer"
            on:click={toggleVisibility}
          >
            <img src="/assets/icon-share.svg" alt="share" />
          </button>
          <div
            class="flex flex-col absolute -right-20 bottom-24 invisible md:peer-focus:visible"
          >
            <div
              class="flex items-center gap-5 bg-cstm-dark-grayish-blue px-10 py-5 rounded-xl"
            >
              <p class="uppercase tracking-[0.4em] text-cstm-grayish-blue">
                Share
              </p>
              <div class="flex items-center gap-5">
                <img
                  src="/assets/icon-facebook.svg"
                  alt="facebook icon"
                  class="cursor-pointer"
                />
                <img
                  src="/assets/icon-twitter.svg"
                  alt="twitter icon"
                  class="cursor-pointer"
                />
                <img
                  src="/assets/icon-pinterest.svg"
                  alt="pinterest icon"
                  class="cursor-pointer"
                />
              </div>
            </div>
            <div
              class="w-16 overflow-hidden inline-block relative left-[118px]"
            >
              <div
                class=" h-5 w-5 bg-cstm-dark-grayish-blue -rotate-45 transform origin-top-left"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
    {#if isVisible}
      <div
        transition:slide
        class={`bg-cstm-dark-grayish-blue text-cstm-grayish-blue px-10 py-9 rounded-b-xl absolute bottom-0 w-full ${visibility} md:hidden`}
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
    {/if}
  </div>
</main>
