<script>
  import { fade } from "svelte/transition";
  import { onMount } from "svelte";
  function* animate() {
    yield 5;
  }
  function isInViewport(el) {
    const rect = el.getBoundingClientRect();
    return (
      rect.top >= 0 &&
      rect.left >= 0 &&
      rect.bottom <=
        (window.innerHeight || document.documentElement.clientHeight) &&
      rect.right <= (window.innerWidth || document.documentElement.clientWidth)
    );
  }
  let visible = true;
</script>

<div class="h-full w-full" id="mobile-howl">
  <div class="sticky top-20 grid align-center background-white">
    <p
      class="pl-2 text-5xl lg:text-8xl text-center all-round-gothic-medium-oblique uppercase spacing"
    >
      HOWL
    </p>
  </div>
  <div
    class="h-fit w-full mt-24 pb-8 grid place-items-center all-round-gothic-medium-oblique overflow-scroll join join-vertical px-4 text-sm leading-tight"
  >
    <div>
      <p>The most pressed button in the world is "skip ad."<br /><br />
        Most of the time they deserve to be skipped. Because they're bad,
        boring, they're just…average.<br /><br />
        Average is a joy killer. Average is a
        waste of everyone's time.<br /><br />
        We're here with a purpose. To give ideas that
        matter, the ones that people love and engage, a bigger chance to exist.<br /><br />
        That's why we're not only an ad agency, we're a production house too.<br /><br />
        We're small, faster and more efficient. <br /><br />
        We're project driven. And we hire accordingly. <br />
        We're here to unleash the kind of work people cannot ignore.
        We're here for the joy of doing what we love. <br /><br />
        We're here for shorter calls and longer relationships.
        We want everyone involved to be happy. <br /><br />
        And occasionally howling
      </p>
    </div>
      <p>
        
      </p>
  </div>
</div>
