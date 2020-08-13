<template>
    <div>
        <form @submit="submit">
            <section>
                <h5></h5>
                <input v-model="form.name" type="text" placeholder="what is your name?" class="form-control form-control-lg">
            </section>
            <section>
                <h5></h5>
                  <input v-model="form.phone" type="tel" placeholder="what is your phone number?" class="form-control form-control-lg">
                  <br>
                  <input v-model="form.email" type="email" placeholder="what is your email?" class="form-control form-control-lg">
            </section>
            <section>
                <h5></h5>
                <textarea v-model="form.message" placeholder="please provide the time you checked in & out"  class="form-control form-control-lg"></textarea>
            </section>
            <section>
                <input v-model="form.table" type="number" placeholder="what is your table number?" class="form-control form-control-lg">
            </section>
            <button @click.prevent="submit">submit</button>
        </form>
    </div>
</template>

<script>
export default {
    name: "submit",
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
    methods: {
        submit(e){
            e.preventDefault();
            const newForm = {

            }
            this.$emit('form', newForm);

        }
    },
}


</script>

<style scoped>

</style>