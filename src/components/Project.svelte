<script>
  export let image;
  export let title;
  // export let description;
  export let projectURL;
  export let projectSource;
</script>

<div class="project">
  <div class="project__image">
    <img  src={image} alt={title} />
  </div>
  <h4>{title}</h4>
  <!-- <p class="project__description">
    {description}
  </p> -->
  <div class="project__btn-box">
    <a href={projectURL}>
      <button class="btn--project"> Demo </button>
    </a>

    <a href={projectSource}>
      <button class="btn--project"> GitHub Repo </button>
    </a>
  </div>
<!-- <hr class="project__post"> -->
</div>

<style lang="scss">
  .project {
    display: flex;
    flex-direction: column;
align-items: center;
    width: 10rem;
    margin: 2rem;
    padding: .5rem;

    &__image{
       & > img{
        width: auto;
        height: 10rem;
       }
    }
    &__btn-box{
        padding-bottom: 1rem;
        text-align: center;

    }
  }

  .btn{
    &--project{
        margin-top: 1rem;
    }
  }
</style>
