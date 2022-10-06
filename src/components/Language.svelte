<script>
  export let url;
  export let language;
</script>

<div class="areas-of-expertise__language">
  <img src={url} alt={language} />
</div>

<style lang="scss">
  @import "../scss/global";
  .areas-of-expertise__language {
    cursor: pointer;
    width: 5rem;
    height: auto;
    margin: 1rem;
    @include transition();
    &:hover {
      @include enlarge();
    }
  }
</style>
