<script>
</script>

<h2 class="nav-header">What would you like to know about me?</h2>

<nav class="selections">
  <a href="#about-me" class="selections__category"> About Me </a>
  <a href="#areas-of-expertise" class="selections__category">
    Areas of Expertise
  </a>
  <a href="#projects" class="selections__category"> Projects </a>
  <a href="#contact-me" class="selections__category"> Contact Me </a>
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

  .nav-header {
    text-align: center;
    margin-top: 2rem;
  }

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
