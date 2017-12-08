<template>
    <div class="loginContainer">
        <Hello :msg = 'msg'></Hello>
    </div>
</template>
<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';
import Hello from '@/components/HelloWorld.vue';

@Component({
    // 引入组件
    components: {
        Hello
    }
})
export default class Login extends Vue {
    msg: String = '登录页';

    mounted() {
        setTimeout(() => {
            this.msg = '变化';
        }, 2000)
    }
    
}
</script>
<style lang="scss">

</style>


