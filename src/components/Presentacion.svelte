<script>
  import foto from '../assets/images/i/original.jpg'
</script>
<section class="grid fix">
  <article>
    <h1>👋🏼 <span>¡Hola!</span> Bienvenid@ a mi sitio web 🌐</h1>
    <p>
      Soy <strong>José</strong>, un desarrollador web rumbo a la especialización
      en el Fronted. Actualmente me encuentro buscando trabajo Jr.
    </p>
  </article>
  <article>
    <figure>
      <img
        src={foto}
        alt="coding"
      
      />
      <p class = "name">José Polanco </p>
    </figure>
  </article>
</section>

<style>

article{


  display: grid;
  place-content: center;
  text-align: center;


}
  h1 {
    font-size: 2rem;
    color: var(--white);
    span {
      color: var(--primary);
    }
  }

  p {
    color: var(--white);
  }
  img{
    border-radius: 50%;
    width: 100%;
    height: 250px;
  }

  .name{
    color: var(--primary);
    font-size: 30px;
    font-weight: 400;
  }
</style>
