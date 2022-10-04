<script>
    import Language from '../components/Language.svelte'
    import stack from '../subscriptions/languages'

</script>

<!--Image sources: https://devicon.dev/-->
    <section class="selected-option areas-of-expertise" id="areas-of-expertise">
       
       <h2 class="areas-of-expertise__heading">
        Areas of Expertise
       </h2>
       <div class="areas-of-expertise__content">
          {#each stack as language}
       <Language language={language.name} url={language.url}/>
       {/each}
       </div>
      
      </section>

      <style lang="scss">
        .areas-of-expertise{
            &__content{
                display: flex;
            flex-direction: row;
            justify-content: space-evenly;
            }
            
        }
      </style>