<template>
    <div>
        <form v-form v-on:submit="sub" @submit.prevent="checkForm">
            <section>
                <h5></h5>
                <input v-model="name" type="text" placeholder="Please fill in your name?" class="form-control form-control-lg">
            </section>
            <section>
                <h5></h5>
                  <input v-model="phone" type="tel" placeholder="Please fill in your phone number?" class="form-control form-control-lg">
                  <br>
                  <input v-model="email" type="email" placeholder="Please fill in your email?" class="form-control form-control-lg">
            </section>
            <section>
                <h5></h5>
                <textarea v-model="message" placeholder="Please provide the time you checked in & out"  class="form-control form-control-lg"></textarea>
            </section>
            <section>
                <input v-model="table" type="number" placeholder="Please fill in your table number?" class="form-control form-control-lg">
            </section>
            <button class="btn-danger">submit</button>
        </form>
    </div>
</template>

<script>
export default {
    name: "Form",
    data() {
    return {
      form: [{
               name:'',
               email: '',
               phone: '',
               message: '',
              table: ''
               }
            ]
    }
    },
    methods: {
        checkForm: function() {
            console.log({name: this.name, email: this.email});
            alert('Processing');
        },
        sub: function(){

        }

        
    /*     submit(e){
            e.preventDefault();
            const newForm = {

            }
            this.$emit('form', newForm);

        } */
    },
}


</script>

<style scoped>

</style>