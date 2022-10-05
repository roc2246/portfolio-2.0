<script>
  import Header from "./sections/Header.svelte";
  import Nav from "./sections/Nav.svelte";
  import AboutMe from './sections/AboutMe.svelte';
  import ProjectsBox from './sections/ProjectsBox.svelte'
  import AreasOfExpertise from './sections/AreasOfExpertise.svelte'
  import Contact from "./sections/Contact.svelte";

</script>

<Header />
<main>
  <!-- <Nav/> -->
  <AboutMe/>
  <AreasOfExpertise />
  <ProjectsBox />

</main>
<hr>

<footer>
<Contact/>

</footer>

<style lang="scss">
  @import './scss/global';
  main{
   @include center();
   display: flex;
   flex-direction: row;
   flex-wrap: wrap;
   justify-content: center;
  }
</style>
