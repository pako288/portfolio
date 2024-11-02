<script>
    import star from '../assets/images/stars.png'
    import cripto from '../assets/images/projects/cripto.png'
    import clima from '../assets/images/projects/clima.png'
    import fono from '../assets/images/projects/fono.png'
    import compras from '../assets/images/projects/compras.png'


    let projects = $state([
        {nombre: `Cotizador de Criptomonedas`,direccion: `https://cotizador-criptomonedas-delta.vercel.app/`, imagen: cripto},
        {nombre: `Lista de Compras`,direccion: `https://listacompras-ten.vercel.app/`, imagen: compras},
        {nombre: `Landing page Fonoaudiologia`,direccion: `https://demo-fonoaudio.vercel.app/`, imagen: fono},
        {nombre: `Aplicación del clima`,direccion: `https://clima-app-sepia.vercel.app/`, imagen: clima},
    ])
</script>

<section>
    <h1>Projects</h1>

    <section class="project">
       {#each projects as item}

      <article>
        <a href={item.direccion} target="_blank">
            <img class="project-image" src={item.imagen} alt="">
        </a>
      </article>
       {/each}

    </section>

    <figure>
        <img class="su-bg" src={star} alt="" >
    </figure>
</section>


<style>
    section{
        height: 100vh;
        position: relative;
        /* background: red; */
    }
    .project{
        height: 90vh;
        background: #ffffff30;
        backdrop-filter: blur(2px);
        border: 1px solid var(--white);
        border-radius: 20px;
        display: grid;
        grid-template-columns: repeat( auto-fit, minmax(min(150px, 100%), 1fr));
        grid-auto-rows: 200px;
        padding: 10px;
        gap: 20px;
    }

    .su-bg{
        position: absolute;
        object-fit: cover;
        bottom: 80px;
        left: 50%;
        transform: translateX(-50%) rotateZ(45deg);
        border-radius: 20px;
        z-index: -1;
    }
    article{
        padding: 0;
        margin: 0;
        border-radius: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: row;
        width: 100%;
        /* background: red; */
        border: 2px solid var(--white);
        overflow: hidden;
       

      & a{
        /* background: #000; */
        height: 100%;
        width: 100%;
        position: relative;
        overflow: hidden;
        text-decoration: none;
        color: var(--primary);

        &::after{
          content: "👆🏼 Visitar proyecto";
          position: absolute;
          display: flex;
          justify-content: center;
          align-items: center;
         
          height: 100%;
          width: 100%;
          background: #030303e8;
          border-radius: 20px;
          z-index: -1;
          transform: scale(0);
          top: 0;
          transition: .5s linear;
          z-index: 1;
        }
        &:hover::after{
    /* transform: translateX(0); */
    transform: scale(1);
  }


        & .project-image{
          width: 100%;
          height: 100%;
          aspect-ratio: 1/1;
        }
      }

    }

</style>

<!-- &::after{
    content: "👆🏼 Visitar proyecto";
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    height: 100%;
    width: 100%;
 background: #030303;
 border-radius: 20px;
 z-index: -1;
 transform: translateX(-100%);
 transition: .5s linear;
 z-index: 1;
  }

  &:hover::after{
    transform: translateX(0);
  } -->