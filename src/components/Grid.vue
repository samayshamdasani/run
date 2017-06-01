<template>

<table class="table">
  <thead>
    <tr>
      <th>Date</th>
      <th>Run</th>
      <th>Time</th>
      <th>Mileage</th>
      <th>Pace</th>
      <th>Feeling</th>
    </tr>
  </thead>
  
  <tbody contentEditable="true" id="table">
    <tr v-for="row in rows">
      <td>Date?</td>
      <td>Describe your run...</td>
      <td v-model="row.time">Time?</td>
      <td v-model="row.mileage">How many?</td>
      <td v-model="row.pace">How fast?</td>
      <td v-model="row.feeling">Feels?</td>
    </tr>
  <a class="button is-danger is-pulled-left" contentEditable="false" style="margin: 2%;" v-on:click="addRow">+</a>
  </tbody>

</table>

</template>

<script>
export default {
  data() {
      return {
        rows: [
          {date: "",run: "",time: "",mileage: "",pace: "",feeling: ""}
        ]  
      }
    },
  methods: {
    addRow: function() {
      this.rows.push({date: "",run: "",time: "",mileage: "",pace: "",feeling: ""})
    }
  }
}

</script>

<style>
* {
  outline: none !important;
}

input[type="text"]{
    width:100%;
    display:block;
}

</style>












