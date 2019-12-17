<template>
    <div class="like">
        <div class="zan">
            <i class="fa fa-heart "
               :class="{red : zanData.isZan}"
               @click="dianZan(zanData.id)"></i>
            <span>{{zanData.count}}</span>
        </div>
    </div>
</template>

<script>
    export default {
        name: "giveLike",
        props: {
            zanData: {
                type: Object,
                default:()=>({})
            },
        },
        data() {
            return {
            }
        },
        methods: {
            dianZan(id) {
                this.$emit('state', id)
            }
        }
    }
</script>

<style lang="scss">
    .like {
        width: 300px;
        margin: 0 auto;
    }
    .zan {
        width: 100%;
        margin: 2px auto 0;
        line-height: 30px;
        border: 1px solid;
        .red {
            color: #f00;
        }
    }

</style>
