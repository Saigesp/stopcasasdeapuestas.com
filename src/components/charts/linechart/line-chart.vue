<template>
    <div class="chart__wrapper">
        <div v-if="title" class="chart__title">{{title}}</div>
        <div ref="chart" :style="{height: `${this.height}px`}"></div>
        <div v-if="source" class="chart__source">{{source}}</div>
    </div>
</template>


<script>
import D3LineChart from './d3.linechart';

export default {
    name: 'line-chart',
    data: function(){
        return {
            chart: {},
        }
    },
    props: {
        config: {
            default: {}
        },
        datum: {
            default: []
        },
        title: {
            default: false
        },
        source: {
            default: false
        },
        height: {
            default: 300,
        }
    },
    mounted: function(){
        this.chart = new D3LineChart(
            this.$refs.chart,
            this.datum,
            this.config
        )
    }
}
</script>


<style lang="scss">
@import '../charts-styles';

.chart{
    &__line--linechart {
        stroke-width: 2px;
    }
}
</style>