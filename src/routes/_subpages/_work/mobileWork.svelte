<script>
  import { content } from "./content.js";
  let expandedItem = null;

  function toggleItem(key) {
    if (expandedItem === key) {
      expandedItem = null;
    } else {
      expandedItem = key;
    }
  }
</script>

<div class="h-full w-full overflow-scroll">
  <div class="sticky top-20 grid align-center bg-white">
    <div
      class="pl-2 text-5xl lg:text-8xl text-center all-round-gothic-medium-oblique uppercase spacing"
    >
      WORK
    </div>
  </div>
  <div
    class="h-fit w-full mt-28 pb-24 grid place-items-center all-round-gothic-xlig-oblique overflow-scroll join join-vertical"
  >
    {#each Object.entries(content) as [key, value]}
      <div class="collapse collapse-plus join-item">
        <input
          type="checkbox"
          name="my-accordion-3"
          checked={expandedItem === key}
          on:change={() => toggleItem(key)}
        />
        <div class="collapse-title uppercase text-3xl min-h-0 leading-4">
          {key}
        </div>
        {#if expandedItem === key}
          <div class="collapse-content text-sm overflow-scroll">
            <!-- svelte-ignore a11y-missing-attribute -->
            <!-- <iframe
              src={value.video}
              frameborder="0"
              allow="autoplay;"
              allowfullscreen
              class="w-full p-0 m-0 py-4 "
            /> -->
            <div style="padding:56.25% 0 0 0;position:relative;">
              <iframe
                src={"https://player.vimeo.com/video/" + value.video + "?h=70d246fdb6&autoplay=1&title=0&byline=0&portrait=0"}
                style="position:absolute;top:0;left:0;width:100%;height:100%;"
                frameborder="0"
                allow="autoplay; fullscreen; picture-in-picture"
                allowfullscreen
              />
            </div>
            <script src="https://player.vimeo.com/api/player.js"></script>
            <p>{@html value.text}</p>
            <p class="font-extrabold all-round-gothic-xlig">
              {value.end}
            </p>
          </div>
        {/if}
      </div>
    {/each}
  </div>
</div>
