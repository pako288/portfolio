<script>
  import light from "../assets/images/light.png";
  import Presentacion from "./Presentacion.svelte";

  let scroll = $state(0);

  $effect(() => {
    const currentScroll = () => {
      scroll = window.scrollY;
    };

    window.addEventListener("scroll", currentScroll);

    return () => {
      window.removeEventListener("scroll", currentScroll);
    };
  });
</script>

<header>
  <nav>
    <a href="">Home</a>
    <a href="">About me</a>
    <a href="">Skills</a>
    <a href="">Projects</a>
    <a href="">Contact me</a>
  </nav>

  <Presentacion/>

  <figure class={scroll > 0 ? "seelight" : "light"}>
    <img src={light} alt="light image" width="200" />
  </figure>
</header>

<style>
  header {
    height: 100dvh;
    overflow: hidden;
    & nav {
        & a {
            text-decoration: none;
            color: var(--primary);
            font-size: 1.5rem;
            margin: 0 10px;
            transition: .4s linear;
            &:hover {
              color: var(--white);
            }
        }
    }
  }
  .light {
    position: absolute;
    right: -40px;
    bottom: 100px;
    z-index: -1;
    opacity: 0;
    transition: .7s linear;
    display: block;
  }
  .seelight {
    position: absolute;
    right: -40px;
    bottom: 100px;
    z-index: -1;

    display: block;
    transition: .4s linear;
    animation: appear 1.2s linear;
  }
  @keyframes appear{
    0% {
      opacity: 0;
  }
  100%{
    opacity: .7;
  }
}
</style>
