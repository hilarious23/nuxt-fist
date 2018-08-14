<!-- /users/*は全部これが表示される -->
<template>
    <div>
        <input type="text" v-model="userId">
        <button @click="onLoadUser">Load User</button>
        <!-- ここにusersフォルダのindex.vueが入る→methodsで_idのindex.vueに変わる -->
        <nuxt-child />
    </div>
</template>

<script>
export default {
    data() {
        return {
           userId: '' 
        }
    },
    methods: {
        onLoadUser() {
            this.$router.push('/users/' + this.userId )
        }
    }
}
</script>

