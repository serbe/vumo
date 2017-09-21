<template>
  <nav class="nav hero is-default has-shadow">
    <div class="container">
      <div class="nav-left">
        <a class="nav-item is-tab" href="/">
          <span class="icon is-medium">
            <i class="fa fa-home"></i>
          </span> &nbsp; Home
        </a>
        <div class="nav-item">
          <p class="control is-expanded">
            <input class="input" type="search" placeholder="Поиск по всем полям" onkeyup="filter(this)">
          </p>
        </div>
      </div>
      <span class="nav-toggle">
          <span></span>
      <span></span>
      <span></span>
      </span>
      <div class="nav-right nav-menu">
        <div class="nav-item">
          <p class="control select">
            <select name="rating" id="rating" onchange="changeRating()">
              <option value="0">Все рейтинги</option>
              <option value="1">&gt;4.7</option>
              <option value="2">&gt;4.5</option>
              <option value="3">&gt;4.3</option>
              <option value="4">&gt;4</option>
              <option value="5">&gt;3</option>
            </select>
          </p>
        </div>
        <div class="nav-item">
          <p class="control select">
            <select class="uk-form-select" data-uk-form-select name="genre" id="genre" onchange="changeGenre()">
              <option value="-1">Все жанры</option>
              <option v-for="(item, key) in genres" v-bind:key="key" value="item">{{ item }}</option>
            </select>
          </p>
        </div>
        <div class="nav-item">
          <p class="control select">
            <select class="uk-form-select" data-uk-form-select name="year" id="year" onchange="changeYear()">
              <option value="-1">Все года</option>
              <option v-for="(item, key) in years" v-bind:key="key" value="item">{{ item }}</option>
            </select>
          </p>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
  export default {
    name: 'vue-navigation',
    data () {
      return {
        active: '',
        years: [],
        genres: []
      }
    },
    methods: {
      toggle () {
        this.active = this.active === '' ? 'is-active' : ''
      }
    }
  }
</script>

<style scoped>
a.is-active {
  border-bottom: 3px solid #363636;
}
</style>
