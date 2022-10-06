<script>
</script>

<header class="hero">
  <h1 class="hero__text">
    <span class="hero__text--primary"> Hi, I'm Riley Childs </span><br />
    <br />
    <span class="hero__text--secondary">
      AKA, Your Next Front-End Developer
    </span><br />
    <br />
    <span class="hero__text--tertiary">Scroll down to find out more...</span>
  </h1>
</header>

<style lang="scss">
  @import "../scss/global";

  .hero {
    background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
      url("../images/background.jpg");
    
      @include wholeScreen();

    &__text {
      text-align: center;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
font-weight: 200;
      &--primary {
        @include fade("fade-in", 5);
      }
      &--secondary {
        @include fade("fade-in", 10);
      }
      &--tertiary {
        @include fade("fade-in", 15);
      }
    }
  }
</style>
