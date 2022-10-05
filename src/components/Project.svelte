<script>
  export let image;
  export let title;
  export let description;
  export let projectURL;
  export let projectSource;
</script>

<div class="project">
  <div class="project__image">
    <img  src={image} alt={title} />
  </div>
  <h4>{title}</h4>
  <p class="project__description">
    {description}
  </p>
  <div class="project__btn-box">
    <a href={projectURL}>
      <button class="btn--project"> Demo </button>
    </a>

    <a href={projectSource}>
      <button class="btn--project"> GitHub Repo </button>
    </a>
  </div>
</div>

<style lang="scss">
  .project {
    display: flex;
    flex-direction: column;

    width: 10rem;
    margin: 2rem;
    &__image{
       & > img{
        width: 10rem;
        height: auto;
       }
    }
  }

  .btn{
    &--project{
        margin-top: 1rem;
    }
  }
</style>
