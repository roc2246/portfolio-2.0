<script>
  import Project from "../components/Project.svelte";
  import projects from "../subscriptions/projects";
</script>

<!--Projects-->
<section class="selected-option projects" id="projects">
  <h2 class="projects__heading">Projects</h2>
  <div class="projects__content">
    {#each projects as project}
      <Project
        image={project.image}
        title={project.title}
        projectURL={project.demo}
        projectSource={project.source}
      />
    {/each}
  </div>
</section>

<style lang="scss">
  .projects {
    width: 100%;
    &__content {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: space-evenly;
    }
  }
</style>
