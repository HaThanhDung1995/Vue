<template>
  <div>
    <ul class="tabs">
      <li @click="changeTab('login')">Dang Nhap</li>
      <li @click="changeTab('register')">Dang Ky</li>
    </ul>
    <div class="login" v-if="tabselected==='login'">
      <h2>Dang Nhap</h2>
      <form>
        <input type="text" placeholder="Ten Dang Nhap"/>
        <input type="password" placeholder="Mat Khau"  />
      </form>
    </div>
    <div class="register" v-else-if="tabselected==='register'">
      <h2>Dang Ky</h2>
      <form>
        <input type="text" placeholder="Ten Dang Nhap" />
        <input type="password" placeholder="Mat Khau" />
        <input type="password" placeholder="Nhap lai Mat Khau" />
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
     tabselected:'login',
    };
  },
  methods:{
    changeTab(selectedTab){
     
        this.tabselected=selectedTab;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tabs {
  margin: 0;
  padding: 0;
}
.tabs li {
  display: inline-block;
  padding: 10px 15px;
  border: 1px solid #000;
}
.login,
.register {
  padding: 15px;
  border: 2px solid blue;
  margin-top: 20px;
}
</style>
