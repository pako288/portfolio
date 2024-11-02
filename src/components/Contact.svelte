<script>
  import contact from "../assets/images/contact.png";

  

  // let mostrarValoresInput = $state([])

 
  
  (function() {
            // https://dashboard.emailjs.com/admin/account
            emailjs.init({
              publicKey: "MZW8W7h3zKmaXFT87",
            });
        })();
  $effect(() => {
   

    window.onload = function() {
            document.getElementById('contact-form').addEventListener('submit', function(event) {
                event.preventDefault();
                // these IDs from the previous steps
                emailjs.sendForm('service_4nuso8z', 'template_ejp31nm', this)
                    .then(() => {
                        console.log('SUCCESS!');
                    }, (error) => {
                        console.log('FAILED...', error);
                    });
            });


        }
  })

  
</script>

<article>
  <figure>
    <img src={contact} alt="contact-background" width="700" />
  </figure>

  <h1>Contact me</h1>

  <form  id="contact-form"  >
    <section class="grid form">
      <label for="asunto"
        >Asunto

        <input type="text" name="asunto" id="asunto" required   />
      </label>
      <label for="email"
        >Email

        <input type="email" name="email" id="email" required    />
      </label>
    </section>

    <textarea name="message" id="message" placeholder="Escriba su mensaje" required ></textarea>
    <input class="enviar" type="submit" value="Enviar" id="button"/>

  </form>
</article>

<!-- {#each mostrarValoresInput as item}
   <p>{item.asunto}</p>
   <p>{item.email}</p>
   <p>{item.msg}</p>
{/each} -->

<style>
  article {
    height: 100vh;
    position: relative;
    margin-top: 120px;
  }
  figure {
    position: absolute;
    bottom: -20px;
    left: 50%;
    z-index: -1;
    transform: translateX(-50%);
  }
form{
    height: 90dvh;
    display: flex;
    flex-direction: column;
    width: 75%;
    place-content: center;
    

}
label{
    width: 100px;
}
  input {
    background: #ffffff40;
    border: 1px solid var(--white);
    border-radius: 20px;
    font-weight: 500;
    color: white;
    outline: none;
    border: none;
    height: 30px;
    width: 300px;
    font-size: 16px;
    padding-left: 10px;
}

textarea {
    resize: none;
    backdrop-filter: blur(5px);
    background: transparent;
    border-radius: 20px;
    font-size: 20px;
    margin-top: 15px;
    width: 98%;
    height: 200px;
    padding: 10px;
}

.enviar{
    margin-top: 20px;
    height: 40px;
    width: 100px;
    border-radius: 20px;
    outline: none;
    border: none;
    align-self: flex-end;
    cursor: pointer;
    background: var(--primary);
    color: var(--black);
    transition: .4s ease-in;
    font-size: 16px;

    &:hover{
      border: 2px solid var(--primary);
      background: black;
      color: var(--primary);
    }
}
</style>
