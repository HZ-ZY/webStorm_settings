<template>
    <sc-dialog :title="`XXXXX`" v-model="propValue" custom-class="${NAME}" width="70vw" top="50px" @close="\$emit('input', false)" @opem='open'>
        <div class="dialog-content pl30 pr30">dialog-content</div>
        <span slot="footer" class="dialog-footer mt30">
            <el-button size="mini" @click="_close">取 消</el-button>
            <el-button size="mini" type="primary" @click="_close">确 定</el-button>
        </span>
    </sc-dialog>
</template>
<script>
export default {
    name:"${NAME}",
    props: {
        value: {
            type: Boolean,
            default: false
        }
    },
    data() {
        return {};
    },
    computed: {
        propValue: {
            get() {
                return this.value;
            },
            set(nval) {
                this.\$emit("input", nval);
            }
        }
    },
    methods: {
        //关闭弹窗
        _close() {
            this.\$emit("input", false);
        },
        //打开痰弹窗触发 //获取接口
        open(){
        },
    }
};
</script>
<style lang="scss" scoped>
.${NAME} {
    .dialog-content {
    }
}
</style>
