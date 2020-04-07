<template>
    <div role="alert" :class="['el-alert',changeAlert,'is-center','is-light']">
        <i :class="['el-alert__icon',changeIcon]"></i>
        <div class="el-alert__content">
            <slot name="title">
                <span class="el-alert__title">{{title}}</span>
            </slot>
            <i class="el-alert__closebtn el-icon-close" @click="clickHandle"></i>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        type:{
            type:String,
            default:'info'
        },
        title:{
            type:String,
            default:'这是一段消息提示的文字'
        }
    },
    computed:{
        changeAlert:function(){
            return 'el-alert--'+this.type;
        },
        changeIcon:function(){
            return 'el-icon-'+this.type;
        }
    },
    methods:{
        clickHandle(){
            this.$emit('defclick');
        }
    }
}
</script>

<style>
@import "https://unpkg.com/element-ui@2.13.0/lib/theme-chalk/index.css";
</style>
