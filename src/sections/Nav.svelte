<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();
</script>

<nav class="selections">
  <a
    href="#about-me"
    class="selections__category"
    on:click={() => dispatch("aboutMe")}
  >
    About Me
  </a>
  <a
    href="#areas-of-expertise"
    class="selections__category"
    on:click={() => dispatch("areasOfExpertise")}
  >
    Areas of Expertise
  </a>
  <a
    href="#projects"
    class="selections__category"
    on:click={() => dispatch("projects")}
  >
    Projects
  </a>
  <a
    href="#contact-me"
    class="selections__category"
    on:click={() => dispatch("contactMe")}
  >
    Contact Me
  </a>
</nav>

<style lang="scss">
  @import "../scss/global";
  $selections: (
    1: 0,
    2: 2,
    3: 4,
    4: 6,
    5: 8,
  );

  .selections {
    margin-left: auto;
    margin-right: auto;

    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-evenly;
    @each $selection, $duration in $selections {
      &__category:nth-child(#{$selection}) {
        @include fade("selections__category", calc(10 - $duration));
      }
    }
  }
</style>
