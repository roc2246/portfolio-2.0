<!--About Me-->
<section class="selected-option about-me" id="about-me">
  <h2 class="about-me__heading">
    A Passion for Challenge, A Knack for Problem-Solving
  </h2>
  <div class="about-me__content">
    <img class="about-me__content--image" src="images/euroCarve.jpg" alt="euroCarve" />
    <p class="about-me__content--text">
      I am a front-end web developer located in beautiful Vermont. My goal is to enter the tech field full
      time. I have a passion for challenge and a knack for problem solving, both on and off the slopes.  
    </p>
  </div>
</section>

<style lang="scss">
  @import "../scss/global";
  
  .about-me {
    &__content {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: space-evenly;
      &--text{
        max-width: 20rem;
      }
    }
  }
</style>
