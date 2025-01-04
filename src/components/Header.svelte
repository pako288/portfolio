<script>
  
  import Presentacion from "./Presentacion.svelte";
import menu from '../assets/images/menu.svg';

  let showMenu = $state(false)
  let langValue = $state("en")



const handleMenu = () => {
  showMenu = !showMenu
  
}
const handleLang = (e) => {
  langValue = e.target.value
  console.log(langValue)
  
}


$effect(() => {
   document.addEventListener('click', e => {
  if(!e.target.classList.contains('menu')){
    showMenu = false
  }
   }) 
    
  
})

</script>

<header id="home">
  <nav class=" {showMenu ? "show-menu" : "nav"}" >
    <a href="#home" >Home</a>
    <a href="#about">About me</a>
    <a href="#skills" >Skills</a>  
    <a href="#projects">Projects</a>
    <a href="#contact" >Contact me</a>
    <!-- <select name="" id="" onchange={handleLang} bind:value={langValue} >
      <option value="en">   EN</option>
      <option value="es">   ES</option>
    </select> -->
  </nav>
  <img onclick={handleMenu}  src={menu} alt="menu" class="menu"  width="40px"/>

  <Presentacion/>
</header>

<style>
  header {
    height: 100dvh;
    overflow: hidden;
    margin: 0;
    padding: 0;

  
    & nav {
      position: fixed;
      width: 100%;
      display: flex;
      justify-content: end;
      top: 0;
      right: 0;
      z-index: 9;
        & a {
            text-decoration: none;
            color: var(--primary);
            font-size: 1.2rem;
            margin: 0 10px;
            transition: .5s linear;
            &:hover {
              color: var(--white);
            }
        }
    }
  }


  .nav{
      padding: 5px;
      border-radius: 10px;
      color: white;
      background: #00000080;
      margin-right: 20px;
  
    

    }

    .menu{
      display: none;
    }

  


  @media (width < 420px) {
    .menu{
      display: inline-block;
      /* background: red; */
      position: fixed;
      top: 0;
      right: 0;
      z-index: 9;
    }

    .nav{
      background: #000000;
      color: white;
      display: flex;
      height: 100%;
      flex-direction: column;
      width: 100%;
      justify-content: space-evenly;
      align-items: center;
      clip-path: polygon(100% 0, 100% 0, 100% 0, 100% 0);
      transition: .6s linear;

    }
    .show-menu{
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
    background: #000000;
      color: white;
      display: flex;
      height: 100%;
      flex-direction: column;
      width: 100%;
      justify-content: space-evenly;
      align-items: center;
      transition: .6s linear;
  }
 
  }

</style>
