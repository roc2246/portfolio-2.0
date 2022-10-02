<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();
</script>

<nav>
  <ul class="selections">
    <li class="selections__category" on:click={() => dispatch("home")}>Home</li>
    <li class="selections__category" on:click={() => dispatch("aboutMe")}>
      About Me
    </li>
    <li
      class="selections__category"
      on:click={() => dispatch("areasOfExpertise")}
    >
      Areas of Expertise
    </li>
    <li class="selections__category" on:click={() => dispatch("projects")}>
      Projects
    </li>
    <li class="selections__category" on:click={() => dispatch("contactMe")}>
      Contact Me
    </li>
  </ul>
</nav>

<style lang="scss">
  @import "../scss/global";
  .selections {
    &__category {
      @include fade("selections__category");
    }
  }
</style>
