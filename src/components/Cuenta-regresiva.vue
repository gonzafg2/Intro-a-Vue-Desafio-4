<template>
  <div class="container">
    <div class="row d-flex flex-column align-items-center">
      <h3>Cuenta Regresiva</h3>
      <div class="my-5 display-3">
        {{ minutos }}:{{ segundos }} {{ unidad }}
      </div>
    </div>
    <div class="row d-flex justify-content-around">
      <button
        @click="clic(btn, btnId)"
        class="btn btn-lg btn-success"
        v-for="(btn, btnId) in btns"
        :key="btnId"
      >
        {{ btn }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "CuentaRegresiva",
  data() {
    return {
      counter: "00:00",
      btns: ["3 s", "1 min", "5 min", "10 min", "30 min"],
      unidad: "min:s",
      minutos: "00",
      segundos: "00",
    };
  },
  methods: {
    clic(btn, index) {
      let btnArray = btn.split(" ");
      let btnValue = parseInt(btnArray[0]);

      if (btnValue < 10) {
        btnValue = "0" + btnValue;
      }

      this.segundos = "00";
      this.minutos = "00";

      try {
        if (index === 0) {
          this.segundos = btnValue;

          let btnValueMili = btnValue * 1000

          setInterval(function(){

          }, btnValueMili)

        } else if (index > 0) {
          this.minutos = btnValue;

          let btnValueMili = btnValue * 60 *1000

          setInterval(function(){
            
          }, btnValueMili)

        }
      } catch (error) {
        console.log(error);
      }

      
    },
  },
};
</script>

<style></style>
