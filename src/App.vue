<template>
  <div class="container">
    <div class="card-wrapper">
      <app-card @data="childData = $event"></app-card>
      <app-card :name="title"></app-card>
      <app-card :name="title"></app-card>
    </div>
    <div>
      <button @click="changeName">Adımı değiştir</button>
      <p>Child component üzerinden gelen veri {{childData}}</p>
    </div>
    <div class="form-wrapper">
      <app-form></app-form>
    </div>
  </div>
</template>

<script>
  import Card from './components/Card.vue';
  import Form from './components/Form.vue';
  export default {
    components : {
      appCard: Card,
      appForm: Form,
    },
    data(){
      return{
        title: "omur",
        childData: ""
      }
    },
    methods: {
      changeName(){
        this.title = "bozdag"
      }
    }
  };
</script>

<style>
  .card-wrapper {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    margin-top: 10rem;
  }
  .form-wrapper {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    margin-top: 10rem;
  }
</style>
