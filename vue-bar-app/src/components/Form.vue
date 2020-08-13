<template>
    <div>
        <form v-form v-on:submit="sub" @submit.prevent="checkForm">
            <section>
                <h5></h5>
                <input v-model="name" type="text" placeholder="what is your name?" class="form-control form-control-lg">
            </section>
            <section>
                <h5></h5>
                  <input v-model="phone" type="tel" placeholder="what is your phone number?" class="form-control form-control-lg">
                  <br>
                  <input v-model="email" type="email" placeholder="what is your email?" class="form-control form-control-lg">
            </section>
            <section>
                <h5></h5>
                <textarea v-model="message" placeholder="please provide the time you checked in & out"  class="form-control form-control-lg"></textarea>
            </section>
            <section>
                <input v-model="table" type="number" placeholder="what is your table number?" class="form-control form-control-lg">
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
            form: 
             [
                {name: null},
                {email: null},
                {phone: null},
                {message: null},
                {table: null}
            ]
        }
    },
    props: ["Form"],
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