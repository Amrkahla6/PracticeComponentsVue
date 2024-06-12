<template>
    <section>
        <form @submit.prevent="submitData">
            <input type="text" placeholder="Your Name" v-model="enterdName">
            <input type="text" placeholder="Your Age" v-model="enterdAge">
            <button>Set User Date</button>
        </form>
   
    </section>
</template>

<script>
    export default{
        emits:['set-data'],
        data(){
            return {
                enterdName : "",
                enterdAge  : ""
            }
        },methods : {
            submitData()
            {
                this.$emit('set-data',this.enterdName,this.enterdAge)
            }
        }
    };
</script>