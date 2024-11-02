<script>
    import ws from '../assets/images/ws.svg'
    import linkedin from '../assets/images/linkedin.svg'
    import github from '../assets/images/github.svg'


    const socials = [
        {image : github, direccion: `https://github.com/pako288`},
        {image : linkedin, direccion: `https://www.linkedin.com/in/jose-polanco-770430207?utm_campaign=share_via&utm_content=profile&utm_medium=android_app`},
        {image : ws, direccion: `https://api.whatsapp.com/send?phone=584126829644&text=Hola%20Jos%C3%A9!%20Mir%C3%A9%20tu%20portfolio%20y%20quiero%20comentarte%20sobre`},
]

</script>

<aside>
    {#each socials as social}
        <figure>
            <a href={social.direccion} target="_blank" rel="noopener noreferrer" >
                <img src={social.image} alt="" height="30">
            </a>
        </figure>
    {/each}
</aside>

<style>
    aside{

        position: fixed;
        height: 130px;
        padding: 5px;
        width: 24px;
        right: 0;
        top: 50%;
        background: #ffffff90;
        border-left: 2px solid var(--primary);
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
        transform: translateY(-50%);
        border-radius: 10px;

        & figure{
            margin: 0;

            & a{
                transition: transform .7s linear;
                & :hover{
                    transform: scale(1.1);
                    transition: .7s linear;
                }
            }
        }
    }
</style>