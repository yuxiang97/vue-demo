<template>
    <div class="like">
        <div class="zan">
            <i class="fa fa-heart "
               :class="{red : zanData.isZan}"
               @click="Zan(zanData.id)"></i>
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
            Zan(id) {
                this.$emit('state', id)
            }
        }
    }
</script>

<style lang="scss">
    .zan {
        width: 100%;
        margin: 5px 0;
        line-height: 30px;
        border: 1px solid;
        .red {
            color: #f00;
        }
    }

</style>
