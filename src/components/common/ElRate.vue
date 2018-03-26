<template>
  <div class="el-rate" role="slider" tabindex="0">
      <span class="el-rate__item" v-for="item in max" :key="item" @click="selectValue(item)">
          <i class="el-rate__icon" :class="[classes[item-1]]" :style="getIconStyle(item)"></i>
      </span>
  </div>
</template>

<script>
// 1 click 确定当前多少分
// 2 mousemove mouseleave
// 3 change
export default {
    data() {
        return {
            currentValue: this.value,
            classMap: {}
        }
    },
    props: {
        colors: {
            type: Array,
            default() {
                return ['red', '#F7BA2A', 'pink']
            }
        },
        highThreshold: {
            type: Number,
            default: 4
        },
        lowThreshold: {
            type: Number,
            default: 2
        },
        iconClasses: {
            type: Array,
            default() {
                return [
                    'el-icon-star-on',
                    'el-icon-star-on',
                    'el-icon-star-on'                                        
                ]
            }
        },
        voidIconClass: {
            type: String,
            default: 'el-icon-star-off'
        },
        value: {
            type: Number,
            default: 0
        },
        max: {
            type: Number,
            default: 5
        }
    },
    name: 'ElRate',
    created() {
        if(!this.value) {
            this.$emit('input', 0);
        }
        this.classMap = {
            voidClass: this.voidIconClass,
            lowClass: this.iconClasses[0],
            mediumClass: this.iconClasses[1],
            highClass: this.iconClasses[2]
        }
    },
    computed: {
        voidClass() {
            return this.classMap.voidClass
        },
        activeClass() {
            return this.getValueFromMap(this.currentValue,this.classMap);
        },
        classes() {
            let result = [];
            let i = 0;
            let threshold = this.currentValue;
            for(;i < threshold; i++) {
                result.push(this.activeClass)
            }
            console.log(i);
            for(;i < this.max; i++) {
                result.push(this.voidClass)
            }
            return result;
        },
        colorMap() {
            return {
                lowColor: this.colors[0],
                mediumColor: this.colors[1],
                highColor: this.colors[2],
                voidColor: this.voidColor,
            }
        },
        activeColor(){
            return this.getValueFromMap(this.currentValue, this.colorMap)
        }
    },
    methods: {
        getValueFromMap(value,map) {
            let result = '';
            if(value <= this.lowThreshold) {
                result = map.lowColor || map.lowClass
            }else if (value >= this.highThreshold) {
                result = map.highColor || map.highClass
            }else {
                result = map.mediumColor || map.mediumClass
            }
            return result;
        },
        selectValue(value) {
            this.$emit('input', value)
        },
        getIconStyle(item) {
            const voidColor = this.colorMap.voidColor;
            return {
                color: item <= this.currentValue ? this.activeColor : voidColor
            }
        }
    },
    watch: {
        value(val) {
            this.currentValue = val;
        }
    }
}
</script>

<style >
.el-rate {
    /* margin-left: 85px; */
    margin-top: -15px;
}
.el-rate .el-rate__item {
    margin-right: -5px;
}
.el-rate .el-rate__icon {
    font-size: 8px;
}
</style>
