<template>
  <div class="container mt-3">
    <Header></Header>
    <!-- <div class="row">
      <div class="col-12"></div>
      <h1>Formulario</h1>
      <img width="100" :src="url" :alt="msg">
    </div>
    <hr> -->

   <Formulario></Formulario>
    <!-- <form @submit.prevent="addUser">
      <div>
        <label>
          Nombre: <input v-model="nombre" type="text" placeholder="Nombre" required/>
        </label>
      </div>
      <div>
        <label>
          Edad: <input v-model="edad" type="number" min="15" max="80" placeholder="Edad" required/>
        </label>
      </div>
      <div>
        <label>
          Correo: <input v-model="correo" type="email" placeholder="mail@mail.com" required/>
        </label>
      </div>
      <button type="submit">Enviar</button>
    </form> -->
  </div>
</template>



<script>
  import Header from '@/components/Header.vue'
  import Formulario from '@/components/Formulario.vue'

  export default {
    // data:() =>({
    //   url:"https://cdn.svgporn.com/logos/vue.svg",
    //   msg: "Vue.js",
    //   nombre:"",
    //   edad: 0,
    //   correo:"" 
    // }),
    components: {
      Header,
      Formulario
    }
  }
</script>



















<!-- directivas en vue -->
<!-- <template>
  <div>
    <h1>Directivas en VUE.JS</h1>
    <hr>
    <span v-text="titulo"></span>
    <br>
    <span> con IT:{{titulo}}</span>
    <br>
    <h2>v-html</h2>
    <h3 v-html="html" ></h3>
    <h3>tu edad es: {{edad}}</h3>

    <h2 v-show="edad >= 18">Mayor de edad</h2>
    <h2 v-show="edad < 18">Menor de edad</h2>

    <button @click="agregar()">Agregar edad</button>
    <button @click="disminuir()">Disminuir</button>
    <hr>
    <h2>v-for</h2>
    <ul>
      <li>{{usuarios[0]}}</li>
      <li>{{usuarios[3]}}</li>
      <li>{{usuarios[2]}}</li>
    </ul>
    <br>Empleado v-for
    <ul>
      <li v-for="(usuario, index) in usuarios">{{index}}:{{usuario}}</li>
    </ul>
    <ul>
      <li v-for="(usuario, index) in usuarios" :key="index">{{index}}:{{usuario}}</li>
    </ul>
    <ul>
      <li v-for="(clave, index) in usuarioss" :key="index">{{index}}:{{clave}}</li>
    </ul>
    <hr>Empleado v-on
    <div @click="click()" class="contenedor">clicks {{clicks}}</div>
    <div @dblclick="click()" class="contenedor">clicks {{clicks}}</div>
  </div>
</template>

<script>
  export default {
    data: () => ({
      titulo: "Hola desde VUE.js 3",
      html: "<h5>soy un h5 dentro de un h3 </h5>",
      edad: 18,
      usuarios: ["Wendy","Fernando","Raul","Jose"],
      usuarioss: {
        nombre:"Juana de Arco"
      },
      clicks:0
    }),
    methods:{
      agregar(){
        this.edad++;
      },
      disminuir(){
        this.edad--;
      },
      click(){
        this.clicks++;
      }

    }


  }
</script>




<style scoped>
  div{
    text-align: center;
    margin: 0px 2rem;
  }

  h2{
    color:tomato;
    font-size: 2rem;
  }

  .contenedor{
    background: pink;
    color: snow;
    font-weight: 400px;
    height: 400px;
  }

</style>

 -->























<!-- tarea----------------------------------------- -->
<!-- <template>

  <div class="container-fluid">

    <nav class="navbar navbar-expand-lg bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img src="./img/luis.svg" width="100px" alt="">
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Luis Enrique Mendez Lezama</a>
            </li>
            <li class="nav-item">
              <a class="nav-link active" href="#">10°</a>
            </li>
            <li class="nav-item">
              <a class="nav-link active" href="#">"A"</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <Tarea>
      <div class="row row-cols-1 row-cols-md-3 g-4">
        <div class="col">
            <div class="card">
              <img src="./img/1.jpg" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="card-title">Camarones</h5>
            <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
              content. This content is a little bit longer.</p>
            </div>
            <div class="card-footer">
              <small class="">$500</small>
            </div>
          </div>
      
        </div>
      <div class="col">
        <div class="card">
          <img src="./img/2.jpg" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Carne</h5>
            <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
              content. This content is a little bit longer.</p>
            </div>
            <div class="card-footer">
              <small class="">$400</small>
            </div>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <img src="./img/3.jpg" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Pizza</h5>
            <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
              content.</p>
          </div>
          <div class="card-footer">
            <small class="">$200</small>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <img src="./img/4.jpg" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Hamburguesa</h5>
            <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
              content. This content is a little bit longer.</p>
          </div>
          <div class="card-footer">
            <small class="">$300</small>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <img src="./img/1.jpg" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Camarones</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
          content. This content is a little bit longer.</p>
        </div>
        <div class="card-footer">
          <small class="">$500</small>
        </div>
      </div>
  
    </div>
  <div class="col">
    <div class="card">
      <img src="./img/2.jpg" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Carne</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
          content. This content is a little bit longer.</p>
        </div>
        <div class="card-footer">
          <small class="">$400</small>
        </div>
    </div>
  </div>
  </div>
  

</Tarea>
  </div>

  <br><br><br><br><br>

  <footer class="footer-distributed">


    <div class="footer-left">

      <img src="./img/luis.svg" width="100px" alt="">

      <p class="footer-links">
        <a href="#" class="link-1">Home</a>

        <a href="#">Blog</a>

        <a href="#">Pricing</a>

        <a href="#">About</a>

        <a href="#">Faq</a>

        <a href="#">Contact</a>
      </p>

      <p class="footer-company-name">Company Name © 2015</p>
    </div>

    <div class="footer-center">

      <div>
        <i class="fa fa-map-marker"></i>
        <p><span>444 S. Cedros Ave</span> Solana Beach, California</p>
      </div>

      <div>
        <i class="fa fa-phone"></i>
        <p>+1.555.555.5555</p>
      </div>

      <div>
        <i class="fa fa-envelope"></i>
        <p><a href="mailto:support@company.com">support@company.com</a></p>
      </div>

    </div>

    <div class="footer-right">

      <p class="footer-company-about">
        <span>About the company</span>
        Lorem ipsum dolor sit amet, consectateur adispicing elit. Fusce euismod convallis velit, eu auctor lacus
        vehicula sit amet.
      </p>

      <div class="footer-icons">

        <a href="#"><img src="./img/social_facebook_fb_35.png" width="20px" alt=""></a>
        <a href="#"><img src="./img/social_instagram_3.png" width="20px" alt=""></a>
        <a href="#"><img src="./img/social_Twitter_78.png" width="20px" alt=""></a>

      </div>

    </div>

  </footer>
</template>



<script>
  import Tarea from '@/components/Tarea.vue'

  export default {
    name: 'App',
    components: {
      Tarea
    }
  }
</script>




















<style scoped>
  @import url(https://fonts.googleapis.com/css?family=Open+Sans:400,500,300,700);

  * {
    font-family: Open Sans;
  }

  section {
    width: 100%;
    display: inline-block;
    background: #333;
    height: 50vh;
    text-align: center;
    font-size: 22px;
    font-weight: 700;
    text-decoration: underline;
  }

  .footer-distributed {
    background: #2CD098;
    box-shadow: 0 1px 1px 0 rgba(0, 0, 0, 0.12);
    box-sizing: border-box;
    width: 100%;
    text-align: left;
    font: bold 16px sans-serif;
    padding: 20px 50px;
  }

  .footer-distributed .footer-left,
  .footer-distributed .footer-center,
  .footer-distributed .footer-right {
    display: inline-block;
    vertical-align: top;
  }

  /* Footer left */

  .footer-distributed .footer-left {
    width: 40%;
  }

  /* The company logo */

  .footer-distributed h3 {
    color: #ffffff;
    font: normal 36px 'Open Sans', cursive;
    margin: 0;
  }

  .footer-distributed h3 span {
    color: lightseagreen;
  }

  /* Footer links */

  .footer-distributed .footer-links {
    color: #ffffff;
    margin: 20px 0 12px;
    padding: 0;
  }

  .footer-distributed .footer-links a {
    display: inline-block;
    line-height: 1.8;
    font-weight: 400;
    text-decoration: none;
    color: inherit;
  }

  .footer-distributed .footer-company-name {
    color: #222;
    font-size: 14px;
    font-weight: normal;
    margin: 0;
  }

  /* Footer Center */

  .footer-distributed .footer-center {
    width: 35%;
  }

  .footer-distributed .footer-center i {
    background-color: #33383b;
    color: #ffffff;
    font-size: 25px;
    width: 38px;
    height: 38px;
    border-radius: 50%;
    text-align: center;
    line-height: 42px;
    margin: 10px 15px;
    vertical-align: middle;
  }

  .footer-distributed .footer-center i.fa-envelope {
    font-size: 17px;
    line-height: 38px;
  }

  .footer-distributed .footer-center p {
    display: inline-block;
    color: #ffffff;
    font-weight: 400;
    vertical-align: middle;
    margin: 0;
  }

  .footer-distributed .footer-center p span {
    display: block;
    font-weight: normal;
    font-size: 14px;
    line-height: 2;
  }

  .footer-distributed .footer-center p a {
    color: lightseagreen;
    text-decoration: none;
    ;
  }

  .footer-distributed .footer-links a:before {
    content: "|";
    font-weight: 300;
    font-size: 20px;
    left: 0;
    color: #fff;
    display: inline-block;
    padding-right: 5px;
  }

  .footer-distributed .footer-links .link-1:before {
    content: none;
  }

  /* Footer Right */

  .footer-distributed .footer-right {
    width: 20%;
  }

  .footer-distributed .footer-company-about {
    line-height: 20px;
    color: #92999f;
    font-size: 13px;
    font-weight: normal;
    margin: 0;
  }

  .footer-distributed .footer-company-about span {
    display: block;
    color: #ffffff;
    font-size: 14px;
    font-weight: bold;
    margin-bottom: 20px;
  }

  .footer-distributed .footer-icons {
    margin-top: 25px;
  }

  .footer-distributed .footer-icons a {
    display: inline-block;
    width: 35px;
    height: 35px;
    cursor: pointer;
    border-radius: 2px;

    font-size: 20px;
    color: #ffffff;
    text-align: center;
    line-height: 35px;

    margin-right: 3px;
    margin-bottom: 5px;
  }

  /* If you don't want the footer to be responsive, remove these media queries */

  @media (max-width: 880px) {

    .footer-distributed {
      font: bold 14px sans-serif;
    }

    .footer-distributed .footer-left,
    .footer-distributed .footer-center,
    .footer-distributed .footer-right {
      display: block;
      width: 100%;
      margin-bottom: 40px;
      text-align: center;
    }

    .footer-distributed .footer-center i {
      margin-left: 0;
    }

  }
</style> -->
 -->






<!-- <template>
  <h1>Componentes en VUE</h1>
  <hr>


  <Card url="https://cdn.svgporn.com/logos/vue.svg" nombre="Vue.js"/>
  <Card url="https://cdn.svgporn.com/logos/vuetifyjs.svg" nombre="Vuetify"/>
  <Card url="https://cdn.svgporn.com/logos/angular-icon.svg" nombre="Angular"/>
  <Card url="https://cdn.svgporn.com/logos/react.svg" nombre="React"/>
  
</template>


<script>
  import Card from "./components/Card.vue"

  export default{
    components:{Card},
  }
</script> -->





<!-- <template>
  <button class="btn btn-info"  @:class="nombreClass"  @click="count++">Click {{ count }} veces</button>  
  <button class="btn btn-danger" @click="count1++">Click {{ count1 }} veces</button>  
  <button class="btn btn-success" @click="count2++">Click {{ count2 }} veces</button>  
</template>


<script type="text/javascript">
  export default{
    data(){
      return{
        count:0,
        count1:0,
        count2:0
      }
    },
    props:{
            nombreClass:{
                String,
            }
        },
  }
  // Vue.component('contador',
  // {
  //   data:function(){
  //     return {count:0}
  //   },
  //   // template:`<button v-on:click="count++">
  //   //           Click {{count}} veces 
  //   //          </button>`
  // }
  // )
</script> -->

<!-- <template>
  <div>
    <card titulo="Vue slots">
      <button @:class="parrafo" @click="parrafo" type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal"></button>
    </card> 
  </div>
</template>

<script>
  import card from "./components/Slot.vue"
  export default{
    components:{
      card
    },
    data(){
      return{
        parrafo:`<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        ...
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>`
      }
    }
  }
</script>



 -->


































<!-----------------------------------primer proyecto---------------------------------- -->
<!-- <script>
  export default{
    data:() => ({
        contador:1,
    }),

    methods:{
      saludar(){
        console.log("Hola 10A | @")
      },

      incrementar(){
        this.contador++;
      },
      decrementar(){
        this.contador--;
      },
      resetear(){
        this.contador = 0;
      }

    }
  }
</script>

<template>
  <nav class="navbar sticky-top navbar-dark bg-dark">
    <div class="container-fluid">
          <a class="navbar-brand h1">Luis Enrique Mendez Lezama 10° "A" DMI</a>       
    </div>
  </nav>
  
  <div class="container">

    <img src="./assets/logo.svg" alt="Logo VUE" width="125" height="125">
    <small>
      <h1>Hola desde VUE.JS 3</h1>
    </small>
    <hr>
    <h2>Contador {{contador}}</h2>
    <button @click="incrementar()">+1</button>
    <button @click="decrementar()">-1</button>
    <button @click="resetear()">Reset</button>
    <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
 
  </div>
</template>

<style scoped>
  .container{
    text-align: center;
  }
  small{
    color: #666;
  }
  h1 {
    font-weight: bolder;
  }
  h2{
    font-size: 2.5rem;
  }
  button{
    cursor:pointer;
    font-size: 1.5rem;
    margin: 0pc 8px;
  }
  nav a{
    margin: auto;
  }
</style> -->