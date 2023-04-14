<template>
    <app>
        <v-toolbar app style="background-color: black;" >
            <v-toolbar-title style="color: white;">INTRAMITES</v-toolbar-title>
            <v-spacer></v-spacer>

            <ul>
            <li>
              <a class="linkheader" href="#inicio" style="color: white;">INICIO</a>
            </li>
      
            <li>
              <a class="linkheader" href="#caracteristicas" style="color: white;">CARACTERÍSTICAS</a>
            </li>
            
            <li>
              <a class="linkheader" href="#nosotros" style="color: white;">NOSOTROS</a>
            </li>
          </ul>
            
            <v-spacer></v-spacer>
    
            <v-btn class="btnHeader" id="btnHeader1" @click="clickear">Iniciar sesión</v-btn>
            <v-btn class="btnHeader" id="btnHeader2" @click="clickear">Registrarse</v-btn>
        </v-toolbar>    
        
        <v-carousel show-arrows="hover" id="inicio">
            <v-carousel-item class="slider">
              <v-card class="mx-auto" max-width="344" variant="outlined" id="card">
                <img src="../assets/images-angel/perfil.png" alt="" id="perfil">
                <v-card-item>
                  <div>
                    <div class="text-overline mb-1">
                      ¿AÚN NO ESTÁS REGISTRADO?
                    </div>
                    <div class="text-h6 mb-1">
                      No pierdas la oportunidad de unirte a intrámites, ahorra tiempo y facilita tus trámites.
                    </div>
                  </div>
                </v-card-item>

                <v-card-actions>
                  <v-btn class="btnsSliders" style="background-color: rgb(250, 216, 80);" @click="clickear">¡Registrate ahora!</v-btn>
                </v-card-actions>
              </v-card> 
            </v-carousel-item>

            <v-carousel-item class="slider">
              <v-card class="mx-auto" max-width="344" variant="outlined" id="card">
                <img src="../assets/images-angel/pc.png" alt="" id="perfil">
                <v-card-item>
                  <div>
                    <div class="text-overline mb-1">
                      ¿YA TIENES UNA CUENTA?
                    </div>
                    <div class="text-h6 mb-1">
                      Con intrámites realiza tus trámites de manera en línea y rápida, sin la necesidad de acudir presencialmente y almacena tus archivos en la nube
                    </div>
                  </div>
                </v-card-item>

                <v-card-actions>
                  <v-btn class="btnsSliders" style="background-color: rgb(250, 216, 80);" @click="clickear">Iniciar sesión</v-btn>
                </v-card-actions>
              </v-card> 
            </v-carousel-item>

            <v-carousel-item class="slider">
              <v-card class="mx-auto" max-width="344" variant="outlined" id="card">
                <img src="../assets/images-angel/download.png" alt="" id="perfil">
                <v-card-item>
                  <div>
                    <div class="text-overline mb-1">
                      DESCARGA AHORA
                    </div>
                    <div class="text-h6 mb-1">
                      Descarga la aplicación para celulares, realiza el trámite en el lugar que quieras sin necesidad de un ordenador (NO DISPONIBLE)
                    </div>
                  </div>
                </v-card-item>

                <v-card-actions>
                  <v-btn class="btnsSliders" style="background-color: rgb(250, 216, 80);"> <img src="../assets/images-angel/iconos/android.png" alt="" class="imgSliderBtn">Android</v-btn>
                  <v-btn class="btnsSliders" style="background-color: rgb(250, 216, 80)"> <img src="../assets/images-angel/iconos/apple.png" alt="" class="imgSliderBtn">iOS</v-btn>
                </v-card-actions>
              </v-card> 
            </v-carousel-item>
        </v-carousel>

        <v-container class="APP" id="caracteristicas">
          <h1 style="margin: 20px; text-align: center;">NUESTRA APLICACIÓN</h1>
            <v-row class="row1">
              
              <!--Esta es una tarjeta-->
              <v-card class="mx-auto">
              <v-title>
                <img src="../assets/images-angel/iconos/estrella.png" alt="" class="icons">
                <h3>Uso sencillo</h3>
              </v-title>
            <v-card-text>
              Se ha diseñado de manera intuitiva de manera que sea facíl hacer uso de esta herramienta.
            </v-card-text>
            </v-card>
           

            <!--Esta es una tarjeta-->
            <v-card class="mx-auto">
              <v-title>
                <img src="../assets/images-angel/iconos/multiplataforma.png" alt="" class="icons">
                <h3>Multiplataforma</h3>
              </v-title>
            <v-card-text>
              Compatibles con todo tipo de dispositivos y cualquier sistema operativo.
            </v-card-text>
            </v-card>


            
            <!--Esta es una tarjeta-->
            <v-card class="mx-auto">
              <v-title>
                <img src="../assets/images-angel/iconos/laptop.png" alt="" class="icons">
                <h3>Portabilidad</h3>
              </v-title>

            <v-card-text>
              Intrámites se adaptan a todo sin necesidad de crear diferentes apps.
            </v-card-text>
            </v-card>


            <v-card class="mx-auto">
              <v-title>
                <img src="../assets/images-angel/iconos/server.png" alt="" class="icons">
                <h3>Servicio al cliente</h3>
              </v-title>
            <v-card-text>
              Intrámites crea un nuevo espacio donde mostrar tus documentos, servicios o contenidos.
            </v-card-text>
            </v-card>

            
            <!--Esta es una tarjeta-->
            <v-card class="mx-auto">
              <v-title>
                <img src="../assets/images-angel/iconos/contacto.png" alt="" class="icons">
                <h3>Contacto rápido</h3>
              </v-title>
            <v-card-text>
              Con este nuevo espacio estarán en contacto con la institución durante la jornada laboral.
            </v-card-text>
            </v-card>

            
            <!--Esta es una tarjeta-->
            <v-card class="mx-auto">
              <v-title>
                <img src="../assets/images-angel/iconos/refresh.png" alt="" class="icons">
                <h3>Actualizaciones</h3>
              </v-title>

            <v-card-text>
              Solución a tipos de error/bug en el sistema, ademas de brindar seguridad a los datos de los usuarios.
            </v-card-text>
            </v-card>
            </v-row>

            
 
          </v-container>

        <v-container  class="Nosotros" id="nosotros">
            <div style="margin: 0px 0px 50px;">
              <h2 style="font-size: 30px; margin-bottom: 20px; text-align: center;">Equipo de intrámites</h2>
              <p style="text-align: center;">Realizado por estudiantes de la Universidad Tecnológica de Salamanca, Guanajuato.</p>
            </div>
            <v-row justify="space-around" id="rowNosotros">
            <v-card width="390" class="cardPerson">
                <div height="200" cover class="text-white">
                  <img class="imgNosotros" src="../assets/images-angel/nosotros/Bryan.jpeg" alt="">
                </div>
                <v-card-text>
                <v-card-tittle>Bryan Coronado</v-card-tittle>
                <v-card-subtitle>DEVELOPER FRONT END</v-card-subtitle>
                <div class="font-weight-bold ms-1 mb-2" style="text-align: justify;">Estudiante en Tecnologías de la Información, Área Desarrollo de Software Multiplataforma de la Universidad Tecnológica de Salamanca. </div>
                </v-card-text>

                <v-card-actions class="actions">
                  <a href="https://www.facebook.com/bryan.coronado.712714" class="redesBtn"><img src="../assets/images-angel/facebook.png" alt="" style="width: 39px;"></a>
                  <a href="https://www.instagram.com/_bryancee_/?hl=es" class="redesBtn"><img href="#" src="../assets/images-angel/instagram.png" alt="" style="width: 39px;"></a>
                </v-card-actions>
            </v-card>

        
            <v-card width="390" class="cardPerson">
                <div height="200" cover class="text-white">
                  <img class="imgNosotros" src="../assets/images-angel/nosotros/Lirachi.jpeg" alt="">
                </div>
                <v-card-text>
                <v-card-tittle>Omar Lirachi</v-card-tittle>
                <v-card-subtitle>DEVELOPER FRONT END | DESIGNER</v-card-subtitle>
                <div class="font-weight-bold ms-1 mb-2" style="text-align: justify;">Estudiante en Tecnologías de la Información, Área Desarrollo de Software Multiplataforma de la Universidad Tecnológica de Salamanca. </div>
                </v-card-text>

                <v-card-actions class="actions">
                  <a href="https://www.facebook.com/profile.php?id=100009579995096" class="redesBtn"><img src="../assets/images-angel/facebook.png" alt="" style="width: 39px;"></a>
                  <a href="https://www.instagram.com/omxrlirxchi/?hl=es" class="redesBtn"><img href="#" src="../assets/images-angel/instagram.png" alt="" style="width: 39px;"></a>
                </v-card-actions>
            </v-card>

            <v-card width="390" class="cardPerson">
                <div height="200" cover class="text-white">
                  <img class="imgNosotros" src="../assets/images-angel/nosotros/Berman.jpeg" alt="">
                </div>
                <v-card-text>
                <v-card-tittle>Gustavo Berman</v-card-tittle>
                <v-card-subtitle>DATA BASE MANAGMENT</v-card-subtitle>
                <div class="font-weight-bold ms-1 mb-2" style="text-align: justify;">Estudiante en Tecnologías de la Información, Área Desarrollo de Software Multiplataforma de la Universidad Tecnológica de Salamanca. </div>
                </v-card-text>

                <v-card-actions class="actions">
                  <a href="https://www.facebook.com/gustavo.bermanespinoza.3" class="redesBtn"><img src="../assets/images-angel/facebook.png" alt="" style="width: 39px;"></a>
                  <a href="https://www.instagram.com/bustabito/?hl=es" class="redesBtn"><img href="#" src="../assets/images-angel/instagram.png" alt="" style="width: 39px;"></a>
                </v-card-actions>
            </v-card>



            <v-card width="390" class="cardPerson">
                <div height="200" cover class="text-white">
                  <img class="imgNosotros" src="../assets/images-angel/nosotros/Soto.jpeg" alt="">
                </div>
                <v-card-text>
                <v-card-tittle>Cristian Soto</v-card-tittle>
                <v-card-subtitle>MOBILE DEVELOPER</v-card-subtitle>
                <div class="font-weight-bold ms-1 mb-2" style="text-align: justify;">Estudiante en Tecnologías de la Información, Área Desarrollo de Software Multiplataforma de la Universidad Tecnológica de Salamanca. </div>
                </v-card-text>

                <v-card-actions class="actions">
                  <a href="https://www.facebook.com/profile.php?id=100004636754728" class="redesBtn"><img src="../assets/images-angel/facebook.png" alt="" style="width: 39px;"></a>
                  <a href="https://www.instagram.com/_criseratops/?hl=es" class="redesBtn"><img href="#" src="../assets/images-angel/instagram.png" alt="" style="width: 39px;"></a>
                </v-card-actions>
            </v-card>


            <v-card width="390" class="cardPerson">
                <div height="200" cover class="text-white">
                  <img class="imgNosotros" src="../assets/images-angel/nosotros/Angel.jpg" alt="" height="150px">
                </div>
                <v-card-text>
                <v-card-tittle>Munoz Castorena</v-card-tittle>
                <v-card-subtitle>DEVELOPER FRONT END</v-card-subtitle>
                <div class="font-weight-bold ms-1 mb-2" style="text-align: justify;">Estudiante en Tecnologías de la Información, Área Desarrollo de Software Multiplataforma de la Universidad Tecnológica de Salamanca. </div>
                </v-card-text>

                <v-card-actions class="actions">
                  <a href="https://www.facebook.com/profile.php?id=100028166203636" class="redesBtn"><img src="../assets/images-angel/facebook.png" alt="" style="width: 39px;"></a>
                  <a href="https://www.instagram.com/eroesay.01/?hl=es" class="redesBtn"><img href="#" src="../assets/images-angel/instagram.png" alt="" style="width: 39px;"></a>
                </v-card-actions>
            </v-card>

            </v-row>

            
            

            
        </v-container>
        
        <v-conteiner>
          <v-footer class="bg-indigo-lighten-1 text-center d-flex flex-column" id="footer">
            <div id="logofooter">
              <img src="../assets/images-angel/logo.png" alt="Logo" id="logoimg">
            </div>

            <v-spacer></v-spacer>

            <div id="contfooter">
              <h4 id="titNos" >Más de nosotros</h4>
              <p id="parrafo" >Proyecto Mexicano, creado y desarrollado por estudiantes de la Universidad Técnologica de Salamanca del Estado de Guanajuato.</p>
            </div>

            <v-spacer></v-spacer>

            <div id="redesfooter">
              <h2 id="titsiguenos">Siguenos</h2>
              <ul>
                <li>
                  <a href="" ><img class="imgIconRedes" src="../assets/images-angel/iconosRedes/facebookRedes.png" alt="" ></a>
                  <a href="" ><img class="imgIconRedes" src="../assets/images-angel/iconosRedes/instaRedes.png" alt=""></a>
                  <a href="" ><img class="imgIconRedes" src="../assets/images-angel/iconosRedes/twitterRedes.png" alt="" ></a>
                  <a href="" ><img class="imgIconRedes" src="../assets/images-angel/iconosRedes/youtubeRedes.png" alt="" ></a>
                </li>
              </ul>
            </div>
          </v-footer>

        </v-conteiner>


        
    <v-content>
        <router-view/>
    </v-content>



</app>
    </template>

    <script>
          export default {
            methods: {
                clickear() {
                    this.$router.push("/login");
                }
            }
          } 

    </script>

    <style scoped>
    
    .btnHeader{
      margin: 11px;
    }
    #btnHeader1{
      background-color: hwb(48 31% 2%);
    }
    #btnHeader1:hover{
      background-color: rgb(136, 111, 11);
    }
    #btnHeader2{
      background-color: rgb(224, 224, 224);
    }
    #btnHeader2:hover{
      background-color: rgb(179, 178, 178);
    }
    .v-responsive__content {
    flex: 1 0 0px;
    max-width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    }
    * {
      font-family: 'Inter', sans-serif;
    }
    .text-overline, mb-1{
      text-align: center;
      margin-bottom: 15px;
    }
    .text-h6, mb-1{
      text-align: center;
      margin: 10px auto;
      width: 90%;
      font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;

    }
    #rowNosotros{
      justify-content: space-around;
    }
    .Nosotros{
      background-image: url(../assets/images-angel/fondos/fondoP2.jpg);
      background-size: cover;
      padding: 10% 20%;
      max-width: 100%;
    }
    .text-white{
      height: 200px;
      background-image: url(../assets/images-angel/fondos/fondo3.jpg);
      display: flex;
    flex-direction: row;
    align-items: center;
    }
    .imgNosotros{
      width: 40%;
      margin: auto;
      border-radius: 100px;
      background-color: orange;
      padding: 10px;
      box-shadow: 5px 6px 9px -3px rgba(64,64,64,0.88);
      -webkit-box-shadow: 5px 6px 9px -3px rgba(64,64,64,0.88);
      -moz-box-shadow: 5px 6px 9px -3px rgba(64,64,64,0.88);
    }
    .cardPerson{
      margin-bottom: 25px;  
      
    }
    .mx-auto{
      width: 370px;
      padding: 10px 20px 20px;
      margin: 5px;
      background-image: url(../assets/images-angel/fondos/fondo3.jpg);

    }
    .row1{
      width: 90%;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    align-content: space-around;
    flex-direction: row;
    justify-content: space-around;
    }
    .row2{
      width: 90%;
      padding: 10px;
      margin: auto;
    }
    .APP{
      background-color: rgb(246, 235, 191);
      background-size: cover;
      padding: 5% 5%;
      max-width: 100%;
      height: 40%px;
    }
    .slider{
      background-image: url(../assets/images-angel/fondos/fondo2.jpg);
      background-size: 100%;
      background-position: center;
      padding-bottom: 5%;
      width: 100%;
      height: 100%;
      background-size: cover;
    }
    .contslider{
      margin: 5% auto;
      width: 30%;
      
      display: grid;
      padding-left: 40px;
      padding-right: 40px;
      text-align: center;
    }
    #titulo{
      margin: auto;
      text-align: center;
    }
    #perfil{
      border-radius: 100px;
      width: 20%;
      margin: auto;
      border-style:groove;
      margin-bottom: 20px;
    }
    .actions{
      width: 30%;
      margin: auto;
      margin-bottom: 10px;
      display: flex;
      flex-direction: row;
      justify-content: center;
     
    }
    .icons{
      width: 50px;
      height: 50px;
    }
    #card{
      box-shadow: none;
      margin: 100px auto;
      background-color: transparent;
      padding: 10px;
      display: flex;
      flex-direction: column;
      background-image: none;
      
    }
    .btnsSliders{
      text-transform:none;
      margin: auto;
      margin-top: 10px;
      background-color: rgb(209, 176, 41);
    }
    .imgSliderBtn{
      width: 25px;
    }
    #inicio{
      display: flex;
    flex-direction: column;
    justify-content: space-around;
    }
    #footer{
      background-color: rgb(0, 0, 0);
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    }
    #logoimg{
      width: 100px;
    }
    #logofooter{
      margin: 1% 1% 1% 5%;
    }
    #contfooter{
      margin: 1% 1% 1% 5%;
    }
    #redesfooter{
      margin: 1% 1% 1% 5%;
    }
    #titNos{
      text-align: center;
      margin-bottom: 15px;
      font-size: 100%;
      color: white;
    }
    #titsiguenos{
      font-size: 100%;
      margin-bottom: 15px;
      margin-top: 20px;
      text-align: center;
      color: white;
    }
    #parrafo{
      text-align: justify ;
      margin: auto;
      width: 70%;
      font-size: 70%;
      color: white;
    }
    .linkheader:link {
      padding: 9px;
      
    }
    .linkheader:focus {
      background: #BAE498;
    }
    .linkheader:hover {
      border-radius: 20px;
      background-color: #CDFEAA;
      
    }
    .linkheader:active {
      background: #265301;
      color: #CDFEAA;
      
    }
    .linkheader{
      border-radius: 20px;
      padding: 8px;
      margin: 10px;
      display: block;
      
      font-size: 100%;
      color: var(--bs-nav-link-color);
      text-decoration: none;
      transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out;
    }
    a{
      color: white;
    }
    ul{
    display: flex;
    flex-direction: row;
    padding-left: 0;
    margin-bottom: 0;
    list-style: none;
    
    }
    li{
      text-align: -webkit-match-parent;
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: space-around;
      align-items: baseline;
    }
    .redesBtn:link {
      border-radius: 200px;
      padding: 5px;
      color: #265301;
    }
    .redesBtn:focus {
      background: #BAE498;
    }
    .redesBtn:hover {
      border-radius: 200px;
      background-color: orange;
    }
    .redesBtn:active {
      background: #265301;
      color: #CDFEAA;
    }
    .redesBtn{
      border-radius: 200px;
      padding: 5px;
      margin: auto;
      
    }
    .imgIconRedes{
      width: 39px; 
      background-color: white; 
      margin: 10px;
      padding: 3px;
      border-radius: 20px;
    }
    
</style>
