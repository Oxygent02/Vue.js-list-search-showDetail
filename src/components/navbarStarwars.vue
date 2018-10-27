<template>
  <div>
    <nav>
      <div class="nav-wrapper">
        <form>
          <div class="input-field">
            <input type="search" v-model="search" @change="doSearch">
            <label class="label-icon" for="search"><i class="material-icons">search</i></label>
            <i class="material-icons">close</i>
          </div>
        </form>
      </div>
    </nav>
  </div>
</template>


<script>
export default {
  data() {
    return {
      search : ""
    };
  },
  methods: {
    doSearch(){
      this.$emit("input-changed", this.search);
    }
  }
};
</script>
