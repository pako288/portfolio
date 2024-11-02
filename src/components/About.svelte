<script>
    import about from '../assets/images/about.png';
    import dev from '../assets/images/dev.svg';
</script>
<article>
    <h1>About me</h1>

    <section class="about">

        <section class="info-about">
            <h3>Un poco sobre mí...</h3>

            <figure>
                <img src={dev} alt="logo dev" width="200">
            </figure>
        </section>
     
        <h4>¡Hola nuevamente! Soy José un chico que descubrio su vocación por la programación. Como ya demanda el mercado,  Me mantengo actualizado respecto a las novedades que surgen sobre la programación web para dar la solución más eficaz y resolver tus problemas mediante código.</h4>
        <p>Hace algunos años sentí pasion por la tecnologia y tras investigar descubri que me gusta la programación. </p>
        <p>Soy autodidacta. Todo el conocimiento que tengo lo he logrado con horas de investigación, documentacion y cursos.</p>
        <p>En mi encontraras un desarrollador incanzable que hará posible tu requerimiento de manera estupenda. Me acoplaré a tu necesidad y planteare la solución a tu petición. </p>
        <!-- <p>Encontraré la solución mas optima tanto en rendimiento y posicionamiento de su servicio deseado ya que me mantengo a la vanguardia de las novedades en el mercado.</p> -->
    </section>

    <figure class="to-bg">
        <img src={about } alt="image" height="800" >
    </figure>
</article>

<style>
    article {
        height: 1000px;
      position: relative;
      overflow: hidden;
      margin-top: 50px;
        h1{
            text-align: center;
          
        }
        .to-bg{
            position: absolute;
            bottom: -40px;
            left: 50%;
            z-index: -1;
        
            transform: translateX(-50%) ;
        }
    }

    .about{
        width: 90%;
        padding: 10px;
        height: 180px;
        overflow: hidden;
        transition: .6s linear;
        interpolate-size: allow-keywords;
        background: #ffffff40;
        border: 1px solid var(--white);
        border-radius: 20px;
        backdrop-filter: blur(10px);
        /* font-weight: 700; */
       

        &:hover{
            height: max-content;
            height: auto;
            
        }

        & h4{
            text-wrap: balance;
        }

        & p{
            text-wrap: pretty;
            color: white;
        }
    }

    .info-about{
        display: flex;
        justify-content: start;
        align-items: center;
    }
</style>