<template>
    <div>
        <active-user :username="users.name" :userage="users.age"></active-user>
        <user-data @set-data="setUserData"></user-data>
    </div>
</template>

<script>
    export default{
        data() {
            return {
                users : {
                    name : "Abed kahla",
                    age  : 28
                }
            }
        },methods : {
            setUserData(name,age)
            {
                // this.users.name = updateName;
                // this.users.age  = updatedAge;
                this.users = {
                    name : name,
                    age  : +age
                }
            }
        }
    };
</script>

<style>
    html{
        font-family: sans-serif;
    }
    section {
        margin: 2rem auto;
        max-width: 40rem;
        border-radius: 12px;
        border: 1px solid #ccc;
        padding: 1rem;
    }
</style>