<template>
  <v-app>
    <v-main>
      <v-card class="mx-auto" width="500" color="red" variant="outlined">
        <v-container>
          <v-card width="100%" height="60" variant="outlined" class="d-flex justify-end align-center"><span class="ml-3 mr-3">{{ pantallita }}</span></v-card>
          <v-row class="mt-2">
            <v-col cols="3">
              <v-btn @click="clickBoton(7)" block color="blue">
                7
              </v-btn>
            </v-col>
            <v-col cols="3">
              <v-btn @click="clickBoton(8)" block color="blue">
                8
              </v-btn>
            </v-col>
            <v-col cols="3">
              <v-btn @click="clickBoton(9)" block color="blue">
                9
              </v-btn>
            </v-col>
            <v-col cols="3">
              <v-btn @click="clickOperacion('+')" block color="red">
                +
              </v-btn>
            </v-col>
          </v-row>

          <v-row>
            <v-col cols="3">
              <v-btn @click="clickBoton(4)" block color="blue">
                4
              </v-btn>
            </v-col>
            <v-col cols="3">
              <v-btn @click="clickBoton(5)" block color="blue">
                5
              </v-btn>
            </v-col>
            <v-col cols="3">
              <v-btn @click="clickBoton(6)" block color="blue">
                6
              </v-btn>
            </v-col>
            <v-col cols="3">
              <v-btn @click="clickOperacion('-')" block color="red">
                -
              </v-btn>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="3">
              <v-btn @click="clickBoton(1)" block color="blue">
                1
              </v-btn>
            </v-col>
            <v-col cols="3">
              <v-btn @click="clickBoton(2)" block color="blue">
                2
              </v-btn>
            </v-col>
            <v-col cols="3">
              <v-btn @click="clickBoton(3)" block color="blue">
                3
              </v-btn>
            </v-col>
            <v-col @click="calcularResultado()" cols="3">
              <v-btn block color="green">
                =
              </v-btn>
            </v-col>
          </v-row>

        </v-container>
      </v-card>
    </v-main>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      pantallita: '',
    };
  },
  methods: {
    clickBoton(numero) {
      this.pantallita = `${this.pantallita} ${numero}`	;
    },
    clickOperacion(operacion) {
      this.pantallita = `${this.pantallita} ${operacion}`;
    },
    calcularResultado() {
      this.pantallita = `${this.pantallita} = ${eval(this.pantallita)}`;
    },
  },
}
</script>
