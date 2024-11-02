<script>
  import { Router, Link, Route } from "svelte-routing";
  import About from "./components/About.svelte";
  import Contact from "./components/Contact.svelte";
import Header from "./components/Header.svelte";
  import Projects from "./components/Projects.svelte";
  import Skills from "./components/Skills.svelte";
  import Socials from "./components/Socials.svelte";



</script>
<main>

  <!-- <Router >
    <nav>
      <Link to="/">Home</Link>
      <Link to="/about">About</Link>
      <Link to="/contact">Contact me</Link>
      <Link to="/skills"> Skills</Link>
    </nav>
    <Route path="/about" component={About} />
    <Route path="/"><Header /></Route>
    <Route path="/contact"><Contact /></Route>  
  </Router> -->




  
  

  
  


  <Header/>
  <About/>
  <Skills />
  <Projects/>
  <Contact/>
  <Socials/>

</main>


