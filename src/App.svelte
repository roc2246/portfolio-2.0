<script>
  import Header from "./sections/Header.svelte";
  import Nav from "./sections/Nav.svelte";

  // Navigation
  let aboutMe = false;
  let areasOfExpertise = false;
  let projects = false;
  let contactMe = false;
</script>

<Header />
<main>
  <Nav
    on:aboutMe={() => (!aboutMe ? (aboutMe = true) : !aboutMe)}
    on:areasOfExpertise={() =>
      !areasOfExpertise ? (areasOfExpertise = true) : !areasOfExpertise}
    on:aprojects={() => (!projects ? (projects = true) : !projects)}
    on:contactMe={() => (!contactMe ? (contactMe = true) : !contactMe)}
  />

  <!--OPTIONS-->

  <h2 class="fade-in">What would you like to know about me?</h2>

  {#if aboutMe == true}
    <!--About Me-->
    <div class="selected-option" id="about-me">
      <h2>Your Friendly Neighborhood Fullstack Developer</h2>
      <div class="about-me-row">
        <img
          class="about-me-image"
          src="images/euroCarve.jpg"
          alt="euroCarve"
        />
        <p class="paragraph-main scroll">
          I am a fullstack web developer located in beautiful Vermont. For over
          twenty years, I have spent most of my time outside living the
          snowboarder life. When off the slopes, I always wanted to dissect and
          break down everything I encoutner in my path.
          <br /><br />Ultimately, I turned to web development to satisfy this
          need. It all started when I began customizing my MySpace page with
          custom HTML and CSS made designs. Eventually, that lead to me taking
          more classes in web development, further solidifying my developer
          skills. Since then, web development and coding became some of the
          biggest passions in my life.
        </p>
      </div>
    </div>
  {/if}

  {#if areasOfExpertise === true}
    <!--Areas of Expertise-->
    <!--Image sources: https://devicon.dev/-->
    <div class="selected-option" id="areas-of-expertise">
      <img class="language" src="https://tinyurl.com/6huwm662" alt="HTML 5" />
      <img class="language" src="https://tinyurl.com/y2pu9scw" alt="CSS 3" />
      <img
        class="language"
        src="https://tinyurl.com/ktbnbrrp"
        alt="JavaScript"
      />
      <img class="language" src="https://tinyurl.com/2prwet54" alt="MySQL" />
      <img class="language" src="https://tinyurl.com/bxxsy6jp" alt="PHP" />
    </div>
  {/if}

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
</style>
