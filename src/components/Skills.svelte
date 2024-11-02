<script>
  // const images = [`html.png`, `css.png`, `js.png` , `git.png` , `boostrap.png`, `react.png`, `svelte.png`]

  import js from "../assets/images/logos-tecnologias/buenos/js.png";
  import html from "../assets/images/logos-tecnologias/buenos/html.png";
  import css from "../assets/images/logos-tecnologias/buenos/css.png";
  import git from "../assets/images/logos-tecnologias/buenos/git.png";
  import react from "../assets/images/logos-tecnologias/buenos/react.png";
  import svelte from "../assets/images/logos-tecnologias/buenos/svelte.png";
  import boostrap from "../assets/images/logos-tecnologias/buenos/boostrap.png";

  const imagenes = [html, css, js, git, boostrap, react, svelte];

  console.log(js);
</script>

<article id="skills" >
  <h1>Skills</h1>
  <article class="grid">
    <section class="first">
      <p>
        Algúnos de los lenguajes que domino para la creación de sitios y
        aplicaciones web
      </p>
      <p>
        En la siguiente sección encontrará algúnos de los proyectos que he
        realizado para demostrar mi conocimiento
      </p>
    </section>
    <section class="skill">
      {#each imagenes as imagen}
        <figure>
          <img src={imagen} alt="" width="100" height="" />
        </figure>
      {/each}
    </section>
  </article>
</article>

<style>
  article {
    height: 100vh;
    width: 100%;
    margin-bottom: 120px;

    h1 {
      padding: 10px;
      padding-top: 20px;
      text-align: center;
      color: inherit;
    }
   

    .first {
      background: url("../assets/images/skills.png");
      background-repeat: no-repeat;
      background-size: cover;
      background-position: 80%;
      height: 90%;
      /* background: red; */
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      flex-direction: column;

      p {
        text-wrap: pretty;
        width: 80%;
        height: max-content;
        padding: 20px 10px;
        margin: 15px 5px;
        background: #ffffff40;
        border: 1px solid var(--white);
        backdrop-filter: blur(10px);
        border-radius: 20px;
        font-weight: 700;
        color: white;
      }
    }
  }

 
  .skill {    
padding: 0;

    height: 90%;
   
    display: grid;
    grid-template-columns: repeat(auto-fill, 90px);
    place-content: center;
    gap: 20px;


    & figure{
      height: 90px;
      width: 100%;
      display: flex;
      place-content: center;
      justify-content: center;
      align-items: center;
      margin: 0;
      position: relative;
      /* padding: 5px; */

   
      &::after, &::before{
        /* --angle: 0deg; */
        content: "";
        position: absolute;
        height: 100%;
        width: 100%;
        background-image: conic-gradient(from var(--angle), transparent 80%, var(--primary), var(--terciary) );
        padding: 2px;
        z-index: -1;
        animation: 3s spin linear infinite;
      }

      &::before{
        filter: blur(1.5rem);
        opacity: 0.5;
      }

   

      & img{
        width: 100%;
        object-fit: cover;
        margin-left: -30px;
        border-radius: 10px;
      
        padding: 0;
        margin: 0;
      }
    }
   
  }
  @property --angle{
    syntax: "<angle>";
    initial-value: 0deg;
    inherits: false;
  }

  @keyframes spin {
    from {
      --angle: 0deg;
    }
    to {
      --angle: 360deg;
    }
  }

 
  
</style>
