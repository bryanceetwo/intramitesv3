<template>
  <v-app id="inspire">
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="8">
            <v-card class="elevation-12">
              <v-window v-model="step">
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 yellow--text text--darken-3"
                        >
                          INTRAMITES
                        </h1>
                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="orange" outlined>
                            <v-icon>fab fa-facebook-f</v-icon>
                          </v-btn>

                          <v-btn class="mx-2" fab color="orange" outlined>
                            <v-icon>fab fa-google-plus-g</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="orange" outlined>
                            <v-icon>fab fa-linkedin-in</v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mt-4">
                          Inicia Sesión con Intramites
                        </h4>
                        <v-form ref="formularioValido">
                          <v-text-field
                            label="Email"
                            name="Email"
                            prepend-icon="email"
                            type="text"
                            color="yellow darken-3"
                            v-model="emailLogin"
                            :rules="emailLoginValidation"
                          />

                          <v-text-field
                            id="password"
                            label="Password"
                            name="password"
                            prepend-icon="lock"
                            type="password"
                            color="yellow darken-3"
                            v-model="passwordLogin"
                            :rules="passwordLoginValidation"
                          />
                        </v-form>
                        <h3 class="text-center mt-4">
                          ¿Olvidaste tu contraseña? Recuperala
                        </h3>
                      </v-card-text>
                      <div class="text-center mt-3">
                        <v-btn
                          rounded
                          color="yellow darken-3 black--text"
                          @click="login"
                          dark
                          >INICIAR SESIÓN</v-btn
                        >
                      </div>
                    </v-col>
                    <v-col cols="12" md="4" class="yellow darken-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1 black--text">
                          ¿No estás Registrado?
                        </h1>
                        <h5 class="text-center black--text">
                          Crea una cuenta ahora
                        </h5>
                      </v-card-text>
                      <div class="text-center" color="black">
                        <v-btn
                          rounded
                          color="black"
                          outlined
                          dark
                          @click="step++"
                          >Registrate</v-btn
                        >
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
                <v-window-item :value="2">
                  <v-row class="fill-height">
                    <v-col cols="12" md="4" class="yellow darken-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1 black--text">
                          ¿Ya una tienes cuenta?
                        </h1>
                        <h5 class="text-center black--text">Conéctate</h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn
                          rounded
                          color="black"
                          outlined
                          dark
                          @click="step--"
                          >Iniciar Sesión</v-btn
                        >
                      </div>
                    </v-col>

                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 yellow--text text--darken-3"
                        >
                          INTRAMITES
                        </h1>
                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="orange" outlined>
                            <v-icon>fab fa-facebook-f</v-icon>
                          </v-btn>

                          <v-btn class="mx-2" fab color="orange" outlined>
                            <v-icon>fab fa-google-plus-g</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="orange" outlined>
                            <v-icon>fab fa-linkedin-in</v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mt-4">
                          Ingresa un correo para Registrarse
                        </h4>
                        <v-form  ref="registro">
                          <v-text-field
                            label="Name"
                            name="Name"
                            prepend-icon="person"
                            type="text"
                            color="yellow darken-3"
                            v-model="name"
                            :rules="nameValidation"
                          />
                          <v-text-field
                            label="Email"
                            name="Email"
                            prepend-icon="email"
                            type="text"
                            color="yellow darken-3"
                            v-model="emailRegister"
                            :rules="emailValidation"
                          />

                          <v-text-field
                            id="password"
                            label="Password"
                            name="password"
                            prepend-icon="lock"
                            type="password"
                            color="yellow darken-3"
                            v-model="passwordRegister"
                            :rules="passwordValidation"
                          />
                        </v-form>
                      </v-card-text>
                      <div class="text-center mt-n5">
                        <v-btn rounded color="yellow darken-3 black--text" dark @click="registrar"
                          >Registrarse</v-btn
                        >
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
              </v-window>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      step: 1,
      nameLogin: "",
      name: "",
      nameValidation: [
        (value) => value.length >= 5 || "Nombre requiere más de 5 caracteres",
      ],
      emailLogin: "",
      emailRegister: "",
      emailValidation: [
        //ESTABLECER REGLAS PARA EL CAMPO
        (v) =>
          !v ||
          /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) ||
          "Debe de ser un dirección de correo válida (Ejemplo: @outlook.com | @gmail.com)",
      ],
      passwordLogin: "",
      passwordRegister: "",
      passwordValidation: [
        (value) =>
          value.length >= 6 ||
          "La contraseña debe incluir al menos 6 caracteres",
      ],

      emailLoginValidation: [
        //ESTABLECER REGLAS PARA EL CAMPO
        (v) =>
          !v ||
          /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) ||
          "Debe de ser un dirección de correo válida (Ejemplo: @outlook.com | @gmail.com)",
      ],
      passwordLoginValidation: [
        (value) =>
          value.length >= 6 ||
          "La contraseña debe incluir al menos 6 caracteres",
      ],
    };
  },
  methods: {
    //<--FUNCIONES
    async login() {
      //<-- MÉTODO QUE SE EJECUTA EL PRESIONAR EL BOTÓN
      const valid = this.$refs.formularioValido.validate(); // <- VALIDA QUE CUMPLA CON LAS REGLAS

      if (valid) {
        const sendData = {
          email: this.emailLogin,
          password: this.passwordLogin,
        };
        await this.$auth
          .loginWith("local", {
            data: sendData,
          })
          .then(async (res) => {
            console.log("respuesta back: ", res);
            if (res.data.alert == "Success") {
              this.$router.push("/dashboard");
            } else if (
              res.data.alert == "Contraseña incorrecta" ||
              "Correo no registrado en la base de datos"
            ) {
              this.$router.push("/login");
            }
          })
          .catch((error) => {
            console.log("error", error);
          });
      } else {
        alert("No cumples con las condiciones, lee los requerimientos");
      }
    },
    async registrar() {

      const valid = this.$refs.registro.validate();

      if(valid){
        const config = {
        headers: {
          "Content-Type": "application/json;charset=UTF-8",
          "Access-Control-Allow-Origin": "*",
        },
      };
      const usuarioNuevo = {
        name: this.name,
        email: this.emailRegister,
        password: this.passwordRegister,
      };
      await this.$axios
        .post("/registro", usuarioNuevo, config)
        .then((res) => {
          console.log("res", res);
          if (res.data.alert == "success") {
            this.$router.push("/dashboard");
          }
        })
        .catch((error) => {
          console.log("error", error);
        });
      }else{
        alert("No cumples con las condiciones, verifica los campos");
      }
      
    },
  },
  props: {
    source: String,
  },
};

import {} from "../plugins/vuetify";
</script>
