<script>
  import Header from "./sections/Header.svelte";
  import Nav from "./sections/Nav.svelte";
  import AboutMe from './sections/AboutMe.svelte';
  import AreasOfExpertise from './sections/AreasOfExpertise.svelte'

  // Navigation
  let aboutMe = false;
  let areasOfExpertise = false;
  let projects = false;
  let contactMe = false;
</script>

<Header />
<main>
  <Nav/>
  <AboutMe/>
  <AreasOfExpertise />


  {#if projects === true}
    <!--Projects-->
    <div class="selected-option" id="projects">
      <div class="project">
        <p class="paragraph-main">
          <img
            class="project-image"
            src="images/projects/after3.png"
            alt="After 3"
          />
          A mockup site of a travel destination page. Included are pages for each
          resort, a randomnly-generated movie of the week, an AJAX powered quiz,
          and much more.<br /><br />
          <a href="http://wh963069.ispot.cc/projects/after3/index.php">
            Check this project out!
          </a> <br />
          <a href="https://github.com/roc2246/after3">Source Code</a>
        </p>
      </div>
      <div class="project">
        <p class="paragraph-main">
          <img
            class="project-image"
            src="images/projects/theCondo.png"
            alt="The Condo"
          />
          An eCommerce site that sells snowboarding softgoods and hardgoods.<br
          /><br />
          <a href="http://wh963069.ispot.cc/projects/eCommerce/index.php">
            Check this project out!
          </a> <br />
          <a href="https://github.com/roc2246/eCommerceMockup">Source Code</a>
        </p>
      </div>
      <div class="project">
        <p class="paragraph-main">
          <img
            class="project-image"
            src="images/projects/reCRUD.png"
            alt="Real Estate App"
          />
          A web application that consumes a self-coded real esate API. CRUD features
          are used to manage the listings.<br /><br />
          <a href="http://wh963069.ispot.cc/projects/real_estate/index.php">
            Check this project out!
          </a> <br />
          <a href="https://github.com/roc2246/real_estate">Source Code</a>
        </p>
      </div>
    </div>
  {/if}

  {#if contactMe === true}
    <!--Contact Me-->
    <div class="selected-option" id="contact-me">
      <form name="contact" method="post">
        <!--Email-->
        <label for="email">Email</label>
        <input type="email" name="email" id="email" /><br />
        <!--Subject-->
        <label for="subject">Subject</label>
        <input type="text" name="subject" id="subject" /><br />
        <!--Message-->
        <label for="message">Message</label><br />
        <textarea rows="15" cols="45" name="message" id="message" /><br />
        <!--Submit Button-->
        <button type="submit" value="Submit" name="submit">Send Message</button>
        <!--PHP Code to Send Email-->
      </form>

      <!--Social Media Links-->
      <div id="social-media">
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
    </div>
  {/if}
</main>

<style lang="scss">
  @import './scss/global';
  main{
   @include center();
  }
</style>
