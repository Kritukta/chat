<template>
  <q-page class="flex flex-center">
    <div>
      <div class="layout-padding">
        <div v-if="!authenticated">
          <div class="column items-center">
            <div class="auto"><img src="~assets/quasar-logo.png"></div>
            <div class="auto">
              <h3>
                <router-link to="/signin">Войти</router-link> или <router-link to="/register">Зарегистрироваться</router-link> в чате
              </h3>
            </div>
            <div class="auto"><img src="~assets/feathers-logo.png"></div>
          </div>
        </div>
        <div v-else class="column items-center">
          <h5>
            <q-checkbox
              v-model="isAdmin"
              color="secondary"
              label="Я администратор"
            />
          </h5>
          <h5>
             <router-link to="/chat">Перейти в чат</router-link>
          </h5>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  props: ['user'],
  data () {
    return {
    }
  },
  computed: {
    authenticated () {
      return this.user !== null
    }
  },
  methods: {
  },
  mounted () {
  },
  beforeDestroy () {
  }
}
</script>

<style lang="styl">

</style>
