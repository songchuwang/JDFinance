<template>
<Panel title="" :class="$style.panel"></Panel>
    
</template>

<script>
import Panel from '../core/panel.vue'
export default{
    components:{
        Panel,
    }

}
    
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel{
    
}

</style>