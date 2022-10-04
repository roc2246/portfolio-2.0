<script>
    import Language from '../components/Language.svelte'

    let stack = [
        {
            name: "HTML 5",
            url: "https://tinyurl.com/6huwm662" 
        }, 
        {
            name: "CSS 3",
            url: "https://tinyurl.com/y2pu9scw" 
        },
        {
            name: "JavaScript",
            url: "https://tinyurl.com/ktbnbrrp" 
        },
        {
            name: "MySQL",
            url: "https://tinyurl.com/2prwet54" 
        },
        {
            name: "PHP",
            url: "https://tinyurl.com/bxxsy6jp" 
        }
    ]
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