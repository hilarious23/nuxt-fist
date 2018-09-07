<!-- /users/*は全部これが表示される -->
<template>
    <div>
        <input type="text" v-model="userId">
        <button @click="onLoadUser">Load User</button>
        <!-- ここにusersフォルダのindex.vueが入る→methodsでrouteして_idのindex.vueに変わる -->
        <nuxt-child />
    </div>
</template>

<script>
import Header from '~/components/Header.vue'

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
    },
    layout: 'users'
}
</script>

