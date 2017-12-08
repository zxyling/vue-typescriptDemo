<template>
  <div class="hello">
    <h2>Essential Links</h2>
    <div class="box" ref="boxs">
        <div class="content">{{msg}}</div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'


@Component({
  props: {
    msg: String
  },
  watch: {
        msg: {
            handler: function() {
                console.log('更新')
            }
        }
    }
})
export default class Hello extends Vue {
    msg: String
    mounted() {
        this.init();
        console.log(this.$refs.boxs);
    }

    init() {
        console.log(1);
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='scss' scoped>



h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.box {
    .content {
        background: red;
    }
}
</style>
