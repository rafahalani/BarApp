<template>
    <div>
        <form @submit.prevent="checkForm">
            <section>
                <h5></h5>
                <input v-model="form.name" type="text" placeholder="Please fill in your name?" class="form-control form-control-lg">
            </section>
            <section>
                <h5></h5>
                  <input v-model="form.phone" type="tel" placeholder="Please fill in your phone number?" class="form-control form-control-lg">
                  <br>
                  <input v-model="form.email" type="email" placeholder="Please fill in your email?" class="form-control form-control-lg">
            </section>
            <section>
                <h5></h5>
                <textarea v-model="form.message" placeholder="Please provide the time you checked in & out"  class="form-control form-control-lg"></textarea>
            </section>
            <section>
                <input v-model="form.table" type="number" placeholder="Please fill in your table number?" class="form-control form-control-lg">
            </section>
            <b-button class="btn-warning" @click="submitForm">submit</b-button>
            
        </form>
    </div>
</template>

<script>
export default {
    name: "Form",
    data() {
    return {
      form: {
               name:'',
               email: '',
               phone: '',
               message: '',
               table: ''
               }
            
    }
    },
    methods: {
        checkForm: function() {
            console.log({name: this.name, email: this.email});
            alert('Processing');
        },
        submitForm: function(){
            this.$emit('SendForm',this.form);
            this.form = '';

        }
    },
}


</script>

<style scoped>

</style>