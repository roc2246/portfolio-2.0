<script>
  import Header from "./sections/Header.svelte";
  import Nav from "./sections/Nav.svelte";
  import AboutMe from './sections/AboutMe.svelte';
  import ProjectsBox from './sections/ProjectsBox.svelte'
  import AreasOfExpertise from './sections/AreasOfExpertise.svelte'

</script>

<Header />
<main>
  <!-- <Nav/> -->
  <AboutMe/>
  <AreasOfExpertise />
  <ProjectsBox />


    

    <!--Contact Me-->
    <!-- <div class="selected-option" id="contact-me">
      <form name="contact" method="post">
        <label for="email">Email</label>
        <input type="email" name="email" id="email" /><br />
        <label for="subject">Subject</label>
        <input type="text" name="subject" id="subject" /><br />
        <label for="message">Message</label><br />
        <textarea rows="15" cols="45" name="message" id="message" /><br />
        <button type="submit" value="Submit" name="submit">Send Message</button>
      </form> -->

      <!--Social Media Links-->
      <!-- <div id="social-media">
        <h4>Social Media</h4>
        <div id="SM-icons">
          <a href="http://www.linkedin.com/in/riley-childs-4b015b1a4">
            <img src="images/socialMedia/linkedIn.png" alt="LinkedIn" />
          </a>
          <a href="https://github.com/roc2246">
            <img src="images/socialMedia/gitHub.png" alt="gitHub" />
          </a>
        </div>
      </div>
    </div> -->
</main>

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
